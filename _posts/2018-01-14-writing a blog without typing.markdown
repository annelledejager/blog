---
layout: post
title:  how to write a blog without typing
date:   2018-01-14 10:10:00
description: how to write a blog using ai in Python - Snowboy, Wit 
comments: true
---

If you're a blogger who's not a writer then you know that writing a blog post can be very time consuming.

The most time consuming part for me is writing the initial draft.

# Imagine you could write a post by just talking about it. How cool would that be? I would write so many more blogs.
<br/>

Luckily for me, the latest buzzword - "AI" could assist me in persuing my lazy blogger's dream. I have to admit, I've never really read up too much about "AI" until now. My colleague suggested using <a href="https://wit.ai/">Wit</a> and <a href="https://snowboy.kitt.ai/">Snowboy</a> for my project. He used both for one of his side projects.

So I decided to give it a go. I chose to write a simple Python script - a <a href="https://github.com/annelledejager/speech-to-text-converter">speech-to-text converter</a> with a hotword detector.

## How it works
<br/>

The converter waits for the hotword before it starts recording. It then records until the hotword is detected again. After that, it does the conversion from speech to text. In short, <b>hotword-speech-hotword</b>, where only the speech gets converted.

The output text is written to an output.txt file. It appends the recordings on new lines. Note that the converter recognizes the words 'comma' and 'full stop' and converts them to ',' and '.'.

## Implementation 
<br/> 

# Speech to text API

The first step is to register to Wit so that you can use their API. You need a unique Wit access token.

{% highlight ruby %}

headers = {
    'Authorization': 'Bearer ' + WIT_ACCESS_TOKEN,
    'Content-Type': 'audio/wav',
}

response = requests.post(URL, data=audio, headers=headers)

data = json.loads(response.content)
text = data.get('_text')

{% endhighlight %}

# Hotword detection

Create a hotword .pmdl file using Snowboy. Their instructions are pretty straight forward. 

To start the hotword detection, use the following code
{% highlight ruby %}

detector = snowboydecoder.HotwordDetector('hotword.pmdl')
detector.start()
detector.terminate()

{% endhighlight %}

# Record speech before hot word detection

Detecting the hotword is easy, but recording and saving the recording before the hotword is detected requires modifying the Snowboy toolkit slightly. 

Snowboy uses a <a href="https://github.com/annelledejager/speech-to-text-converter/blob/master/snowboy/snowboydecoder.py#L25">ring buffer</a> to save the recorded audio and to detect the hotword. It clears the ring buffer after a hotword check is completed. This repeats. For this reason we can't use the ring buffer to hold the whole speech. We need to add a second ring buffer which never clears so that we can retrieve the complete recording ready for conversion to text. 

Find the modifications <a href="https://github.com/annelledejager/speech-to-text-converter/blob/master/snowboy/snowboydecoder.py#L188">here</a>.

# Prerequisite

A prerequisite is <a href="https://github.com/rabitt/pysox">Pysox</a>. We require it to transform the raw data obtained from the ring buffer to a .wav file. The Wit API accepts .wav files. You can find the conversion code <a href="https://github.com/annelledejager/speech-to-text-converter/blob/master/snowboy/snowboydecoder.py#L195">here</a>.

{% highlight ruby %}

self.tfm = sox.Transformer()
self.tfm.set_input_format(rate=16000, bits=16, channels=1, encoding='signed-integer')

self.tfm.build('audio.raw', 'output.wav')

{% endhighlight %}

# Using the speech converter

 The output text is written to output.txt. The text gets apended at the end the file unless you specify a flag `-c` to indicate that you would like to clear the output file before recording. 

 This is just a sample implementation. Run the following commands after cloning the repository to try it!

After activating the virtual environment, run the converter Python script.

{% highlight ruby %}

python speech_to_text_converter.py

{% endhighlight %}

The converter accepts input flag `-c` to clean the output.txt before the next recording. 

{% highlight ruby %}

python speech_to_text_converter.py -c  

{% endhighlight %}

Example output

{% highlight ruby %}

Listening... Press Ctrl+C to exit
INFO:snowboy:Keyword 1 detected at time: 2018-01-14 15:33:37
INFO:snowboy:Keyword 1 detected at time: 2018-01-14 15:34:29
Converting...
Speech converted


{% endhighlight %}

#### This post was written using the speech to text converter.
<br/> 

I will admit that I can't see myself using this project to write all my future posts. Its accuracy isn't very high or perhaps my accent is throwing the API off. Nonetheless, I had to rewrite a lot of the converted text. 

It was an interesting introduction to "AI" though. I thoroughly enjoyed the project.
 
