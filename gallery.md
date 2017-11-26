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
    template: '<div class="story "><div class="thumbnail"><img src="{{image}}" /></div></div>',
    limit -1,
  });
  userFeed.run();
</script>
{% endraw %}
