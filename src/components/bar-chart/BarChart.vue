<template>
  <zingchart :data="myData" :series="mySeries"></zingchart>
</template>

<script>
export default {
  data() {
    return {
      myData: {
        type: 'bar',
        plotarea: {
          'adjust-layout': true
        },
        'scale-x': {
          labels: [
            'Jan',
            'Feb',
            'March',
            'April',
            'May',
            'June',
            'July',
            'Aug',
            'Sep',
            'Oct',
            'Nov',
            'Dec'
          ] /* Scale Labels */
        }
      },

      mySeries: [
        {
          values: [20, 40, 25, 50, 15, 45, 33, 34, 40, 13, 55, 42],
          'background-color': '#e95957'
        },
        {
          values: [5, 30, 21, 18, 59, 50, 28, 33, 55, 21, 18, 38],
          'background-color': '#17c7bf'
        }
      ]
    };
  }
};
</script>

<style></style>
