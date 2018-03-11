<template src="./index.html"></template>

<script>
export default {
  head: {
    script: [
      { src: '/js/utils.js', body: true }
    ],
  },
  mounted: function() {
    setTimeout(() => {
      $(".loading-inner").fadeOut(function() {
        $(".loading-overlay").fadeOut("slow");
      });
    }, 1000);
  }
}
</script>

<style></style>
