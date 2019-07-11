### slick
---
https://github.com/kenwheeler/slick

```sh
bower install --save slick-carousel
npm install slick-carousel
```

```js
$(".slider").slick({
  infinite: false,
  responsive: [{
    breakpoint: 1024,
    settings: {
      slidesToShow: 3,
      infinite: true
    }
  },{
    breakpoint: 600,
    settings: {
      slidesToShow: 2,
      dots: true
    }
  },{
    breakpoint: 300,
    settings: "unslick"
  }]
});

$('.your-element').on('swipe', function(event, slick, direction){
  console.log(directoin);
});
$('.your-elemnet').on('edge', function(event, slick, direction){
  console.log('edge was hit')
});
$('.your-element').on('beforeChange', function(event, slick, currentSlide, nextSlide){
  console.log(nextSlide);
});

$('.your-element').slick('slickAdd', "<div></div>");
var currentSlide = $('.your-element').slick('slickCurrentSlide');
$('.your-element').slick('setPosition');

$(element).slick({
  dots: true,
  speed: 500
});

$(element).slick('slickSetOption', 'speed', 5000, true);
$(element).slick('unslick');
```

```
<link rel="stylesheet" type="text/css" href="//cdn.jsdelivr.net/gh/kenwheeler/slick@1.9.0/slick/slick.css"/>
<link rel="stylesheet" type="text/css" href="//cdn.jsdelivr.net/gh/kenwheeler/slick@1.9.0/slick/slick-theme.css"/>

<div data-slick='{"slidesToShow": 4, "slidesToScroll": 4}'>
  <div><h3></h3></div>
</div>
```
