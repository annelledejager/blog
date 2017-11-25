---
layout: page
permalink: /gallery/
title: gallery
description: a collection of happy moments
---
<div id="instafeed">
</div>
<script src="https://cdnjs.cloudflare.com/ajax/libs/instafeed.js/1.4.1/instafeed.min.js"></script>
<script type="text/javascript">
  var userFeed = new Instafeed({
    get: 'user',
    userId: '709888312',
    clientId: '1bf1e67d24f54cef9f132f19ecf30c94',
    accessToken: '709888312.1677ed0.643556082f774753907aefb0c411681a',
    resolution: 'standard_resolution',
	template: '<div class="columns small-6 medium-4 large-3"><div class="instagram-image-wraper"><a class="test" href="{{link}}"><img src="{{image}}" /></a></div></div>',
    sortBy: 'most-recent',
    limit: 12,
    links: false
  });
  userFeed.run();
</script>

