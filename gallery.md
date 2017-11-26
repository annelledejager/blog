---
layout: page
permalink: /gallery/
title: gallery
description: a collection of happy moments
---

<div id="instafeed">
</div>

{% raw %}
<script type="text/javascript">
  var userFeed = new Instafeed({
    get: 'user',
    userId: '709888312',
    accessToken: '709888312.1677ed0.643556082f774753907aefb0c411681a',
    template: '<div class="thumbnail">{{location}}<br/>{{caption}}<br/>&hearts; {{likes}}<a href="{{link}}" target="_blank"><img src="{{image}}" /></div>',
    limit: 300,
  });
  userFeed.run();
</script>
{% endraw %}
