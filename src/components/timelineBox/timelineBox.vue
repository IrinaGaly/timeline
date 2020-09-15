<template>
  <div class="timeline-component">
    <ul class="timeline-component__list">
      <li class="timeline-component__item" 
      v-for="timeline in sortedList" 
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

  data() {
    return {
      timelines: []
    }
  },

  created() {
    this.timelines = require("../../data/timeline.json");
  },

  computed: {
    sortedList: function() {
      function compare(a, b) {
        if (a.registered < b.registered)
          return -1;
        if (a.registered > b.registered)
          return 1;
        return 0;
      }
        return this.timelines.slice().sort(compare)
    }

  }
}
</script>

<style lang="postcss" scoped src="./timelineBox.pcss">
  
</style>