<template src="./index.html"></template>

<script>
export default {
  head: {
    script: [
      { src: '/js/utils.js', body: true },
    ],
  },
  mounted: function() {
    setTimeout(() => {
      $(".loading-inner").fadeOut(function() {
        $(".loading-overlay").fadeOut("slow");
      });
    }, 1000);

    $('.features-slider').owlCarousel({
        responsive: {
            0: {
                items: 1
            },
            400: {
                items: 1
            },
            600: {
                items: 1
            },
            1000: {
                items: 1
            }
        },
        loop: true,
        margin: 0,
        autoplay: true,
        dots: false,
        nav: false,
        mouseDrag: false,
        touchDrag: false,
        autoplayTimeout: 10000
    });
  }
}
</script>

<style></style>
