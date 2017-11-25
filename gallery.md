---
layout: page
permalink: /gallery/
title: gallery
description: a collection of happy moments
---

<script type="text/javascript">
    var feed = new Instafeed({
        // get: 'tagged',
        // tagName: 'berlin',
        // accessToken:'709888312.1677ed0.643556082f774753907aefb0c411681a',
        // clientId: '1bf1e67d24f54cef9f132f19ecf30c94'

        get: 'user',
	    userId: '709888312',
	    clientId: '1bf1e67d24f54cef9f132f19ecf30c94',
	    accessToken:'709888312.1677ed0.643556082f774753907aefb0c411681a',
	    resolution: 'low_resolution',
	    template: '<div class="columns small-6 medium-4 large-3"><div class="instagram-image-wraper"><a class="test" href="{{link}}"><img src="{{image}}" /></a></div></div>',
	    limit: 12,
    });
</script>

<div id="instafeed"></div> 
