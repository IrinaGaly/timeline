<template>
  <div class="timeline-component">
    <ul class="timelines__list">
      <li class="timelines__item" 
      v-for="timeline in timelines" 
      :key="timeline.id">
        <singleTimeline :timeline="timeline"/>
      </li>
    </ul>
 
  </div>
</template>

<script>
import singleTimeline from "./../singleTimeline/singleTimeline"



export default {
  components: {
    singleTimeline
  },
  
  created() {
    this.timelines = require("../../data/timeline.json");
   }
}
</script>

<style lang="postcss" src="./timeline.pcss">
  
</style>