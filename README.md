## Welcome to eStoreSpeedOptimization.com code file. Feel free to use the code below to help you optimize your Shopify stores speed.

Lazyload background images
------

1. Add data-bg attribute with image url to element ```<div data-bg="{{ 'veggies.jpg' | file_img_url: 'master' }}"></div>```
2. Add lazyload class ```<div class="lazyload" data-bg="{{ 'veggies.jpg' | file_img_url: 'master' }}"></div>```

Lazyload video element (only play when scrolled into view)
------

1. Add lazyload class to video element ```<video class="lazyload"></video>```
2. Add video attributes: preload="none", muted, autoplay, controls ```<video class="lazyload" preload="none" muted autoplay controls data-poster="poster.jpg" src="https://archive.org/download/Popeye_forPresident/Popeye_forPresident_512kb.mp4" type="video/mp4"></video>```

Lazyload iFrame
-------

1. Add lazyload class to iframe element ```<iframe class="lazyload"></iframe>```
2. Add data-src attribute with video url to iframe element ```<iframe class="lazyload" width="560" height="315" data-src="https://www.youtube.com/embed/BADxzcJ5XRU"</iframe>```
3. Maybe you will need to add parameters to the video to make it autoplay e.g. &autoplay=1&mute=1 ```<iframe class="lazyload" width="560" height="315" data-src="https://www.youtube.com/embed/BADxzcJ5XRU?&autoplay=1&mute=1" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>````

Container element autosize to fit background image formula
-------
(img-height / img-width * container-width) e.g. (853 / 1280 * 100) 

Fade effect to lazyloading images
-------
After lazysizes script add the code below
``` <style>
    /* fade image in after load */
.lazyload,
.lazyloading {
	opacity: 0;
}
.lazyloaded {
	opacity: 1;
	transition: opacity 300ms;
}
  </style>
