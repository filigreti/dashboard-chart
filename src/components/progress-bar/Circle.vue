<template>
  <radial-progress-bar
    :diameter="Diameter"
    :completed-steps="completedSteps"
    :total-steps="totalSteps"
    :startColor="color"
    :stopColor="colorTwo"
    :strokeWidth="width"
    :innerStrokeColor="background"
  >
    <div class="text-black-one">{{ completedSteps }}%</div>
    <div class="text-black-two">REMAINING</div>
  </radial-progress-bar>
</template>

<script>
import RadialProgressBar from 'vue-radial-progress';

export default {
  props: {
    Diameter: Number,
    completedSteps: Number,
    color: String,
    colorTwo: String,
    width: Number,
    background: String
  },
  data() {
    return {
      totalSteps: 100
    };
  },
  components: {
    RadialProgressBar
  }
};
</script>

<style>
.text-black-one {
  color: black;
  font-weight: 600;
  font-family: 'Source Sans Pro', sans-serif;
  font-size: 16px;
}
.text-black-two {
  color: black;
  font-weight: 600;
  font-family: 'Source Sans Pro', sans-serif;
  font-size: 12px;
  padding-top: 2px;
}
</style>
