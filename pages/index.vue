<template src="./index.html"></template>

<script>
export default {
  head: {
    script: [
      { src: 'https://cdnjs.cloudflare.com/ajax/libs/Chart.js/2.5.0/Chart.min.js', body: true },
      { src: '/js/utils.js', body: true },
    ],
  },
  mounted: function() {
    setTimeout(() => {
      $(".loading-inner").fadeOut(function() {
        $(".loading-overlay").fadeOut("slow");
      });
    }, 1000);

    new Chart(document.getElementById("doughnut-chart-token"), {
        type: 'doughnut',
        data: {
          labels: ["Token Sale", "Founders and Team", "Advisors", "Bounty", "Reserved"],
          datasets: [
            {
              label: "Token Distribution",
              backgroundColor: ["#3e95cd", "#8e5ea2","#3cba9f","#e8c3b9","#c45850"],
              data: [65,12,6,5,12]
            }
          ]
        },
        options: {
          legend: { position: 'bottom' }
        }
      });

      new Chart(document.getElementById("doughnut-chart-funds"), {
          type: 'doughnut',
          data: {
            labels: ["Development", "Marketing", "Operations", "Legal & Adminitrative"],
            datasets: [
              {
                label: "Token Sale",
                backgroundColor: ["#3e95cd", "#8e5ea2","#3cba9f","#e8c3b9","#c45850"],
                data: [40,35,20,5]
              }
            ]
          },
          options: {
          legend: { position: 'bottom' }
        }
      });
  }
}
</script>

<style></style>
