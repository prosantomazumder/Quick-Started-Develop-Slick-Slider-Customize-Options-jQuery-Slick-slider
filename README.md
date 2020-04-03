# Quick Started Develop Slick-Slider Customize Options jQuery Slick slider

**Live Demo**
[repositories.presstechit-institute.com](http://repositories.presstechit-institute.com/Quick-Started-Develop-Slick-Slider-Customize-Options-jQuery-Slick-slider/)




### Slider HTML Markup 

```
        <!-- SLIDER AREA START -->
        <div id="slider" class="slider-area">
            <div class="slider-active">
                
                <!-- SINGLE SLIDE ITEAM START-->
                <div class="single-slider slide-height d-flex align-items-center" style="background-image:url(social/sliderbg.jpg); background-size: cover; background-position: center center; background-repeat: no-repeat;" data-black-overlay="5">
                    <div class="container">
                        <div class="row">
                            <div class="col-xl-10">
                                <!-- SIDER CONTENT START -->
                                <div class="slide-content text-left">
                                    <h1 data-animation="fadeInUp" data-delay=".5s">Caring for all your Family’s <span>Need helps.</span></h1>
                                    <p data-animation="fadeInUp" data-delay="1s">Lorem ipsum dolor sit amet consectetuer adipiscing elit sed diam nonummy nibh euismod tincidunt ut laoreet dolore magna aliquam erat volutpat. Ut wisi enim ad minim veniam quis nostrud exerc</p>
                                    <div class="read-more">
                                        <a href="#" data-animation="fadeInUp" data-delay="1.5s">About Us
                                            <i class="fa fa-address-card-o"></i>
                                        </a>
                                        <a href="#" data-animation="fadeInUp" data-delay="1.8s">More Info
                                            <i class="fa fa-paper-plane-o"></i>
                                        </a>
                                    </div>
                                </div>
                                <!-- SIDER CONTENT END -->
                            </div>
                        </div>
                    </div>
                </div>
                <!-- SINGLE SLIDE ITEAM END -->
            </div>
        </div>
```


### SLICK SLIDER active.js

```
    function mainSlider() {
        var BasicSlider = $('.slider-active');
        BasicSlider.on('init', function (e, slick) {
            var $firstAnimatingElements = $('.single-slider:first-child').find('[data-animation]');
            doAnimations($firstAnimatingElements);
        });
        BasicSlider.on('beforeChange', function (e, slick, currentSlide, nextSlide) {
            var $animatingElements = $('.single-slider[data-slick-index="' + nextSlide + '"]').find('[data-animation]');
            doAnimations($animatingElements);
        });
        BasicSlider.slick({
            autoplay: true,
            autoplaySpeed: 10000,
            dots: true,
            fade: true,
            prevArrow: '<button type="button" class="slick-prev"><i class="fa fa-long-arrow-left"></i></button>',
            nextArrow: '<button type="button" class="slick-next"><i class="fa fa-long-arrow-right"></i></button>',
            arrows: true,
            responsive: [
                { breakpoint: 767, settings: { dots: false, arrows: false } }
            ]
        });

        function doAnimations(elements) {
            var animationEndEvents = 'webkitAnimationEnd mozAnimationEnd MSAnimationEnd oanimationend animationend';
            elements.each(function () {
                var $this = $(this);
                var $animationDelay = $this.data('delay');
                var $animationType = 'animated ' + $this.data('animation');
                $this.css({
                    'animation-delay': $animationDelay,
                    '-webkit-animation-delay': $animationDelay
                });
                $this.addClass($animationType).one(animationEndEvents, function () {
                    $this.removeClass($animationType);
                });
            });
        }
    }
    mainSlider();
```


### Ask Any Question or if you need help contact me 24/7 we are ready support team.

[Facebook:](https://www.facebook.com/PMPROSANTA0)<br />
[Web:](http://presstechit-institute.com/)\
[Personal:](http://pm-prosanto.themefusions.com/)\
[Email Me:](mailto:prosantomazumder@gmail.com)\
[Linkedin:](https://www.linkedin.com/in/prosantomazumder/)\
[Twitter:](https://twitter.com/prosantomazumd1)\
[Instagram:](https://www.instagram.com/prosantomazumder/)\
[Codepen:](https://codepen.io/ProsantaMazumder)


### Changelog
- [x] Version 1.0.3

##### Cradit
[Bootstrap](https://getbootstrap.com/)
[FontAwesome](https://fontawesome.com/v4.7.0/)
[Animate Css](https://daneden.github.io/animate.css/)
[slick](https://kenwheeler.github.io/slick/)

