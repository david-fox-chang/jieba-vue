<template>
  <div>
    <loading-progress
      :progress="progress"
      :indeterminate="indeterminate"
      :counter-clockwise="counterClockwise"
      :hide-background="hideBackground"
      size="64"
      rotate
      fillDuration="2"
      rotationDuration="1"
    />
    <hr>
    <loading-progress
      :progress="progress"
      :indeterminate="indeterminate"
      :counter-clockwise="counterClockwise"
      :hide-background="hideBackground"
      shape="semicircle"
      size="64"
    />
    <hr>
    <loading-progress
      :progress="progress"
      :indeterminate="indeterminate"
      :counter-clockwise="counterClockwise"
      :hide-background="hideBackground"
      shape="M10 80 C 40 10, 65 10, 95 80 S 150 150, 180 80"
      size="180"
      fill-duration="2"
    />
  </div>
</template>

<script>
import VueProgress from 'vue-progress-path';

export default {
  components: {
    'loading-progress': VueProgress,
  },
  data: () => ({
    progress: '50%',
    indeterminate: 0,
    counterClockwise: 0,
    hideBackground: 0,
  }),
};
</script>

<style lang="less" scoped>
@import (reference) './vue-progress-path.css';
</style>
