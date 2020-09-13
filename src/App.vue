<template>
  <div class="timeline">
    <div class="container">
      <timelineBox />
    </div>
  </div>
</template>

<script>
import timelineBox from "./components/timelineBox/timelineBox"

export default {
  name: 'app',
  components: {
    timelineBox
  }
}
</script>

<style lang="postcss" src="./style.pcss">
  
</style>
