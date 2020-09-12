<template>
  <div class="timeline-component">
    <ul class="timelines__list">
      <li class="timelines__item" v-for="timeline in timelines" :key="timeline.id">
        <singleTimeline :timeline="timeline"/>
      </li>
    </ul>
 
  </div>
</template>

<script>
import singleTimeline from "./../singleTimeline/singleTimeline"

const timelines = [
  {
    "id": "5d820c33647310e4a4f9845c",
    "name": "Chang",
    "about": "Amet mollit ea ullamco magna nisi sint in nulla fugiat ullamco. Commodo et ex excepteur magna et officia sunt. Voluptate officia non anim nostrud in esse minim ex sint. Officia excepteur excepteur sint voluptate ea ea laborum eu reprehenderit. Nulla nisi aliquip sunt aliquip incididunt ea elit laborum ad id sunt ipsum consequat. Ex voluptate ex laboris aliquip.",
    "registered": "Thursday, June 20, 2019 4:17 AM",
    "tags": "eiusmod"
    
  },
  {
    "id": "5d820c335861d73a733a458f",
    "name": "Chang",
    "about": "Amet mollit ea ullamco magna nisi sint in nulla fugiat ullamco. Commodo et ex excepteur magna et officia sunt. Voluptate officia non anim nostrud in esse minim ex sint. Officia excepteur excepteur sint voluptate ea ea laborum eu reprehenderit. Nulla nisi aliquip sunt aliquip incididunt ea elit laborum ad id sunt ipsum consequat. Ex voluptate ex laboris aliquip.",
    "registered": "Thursday, June 20, 2019 4:17 AM",
    "tags": "eiusmod"
  }
]

export default {
  components: {
    singleTimeline
  },

  data() {
    return {
      timelines
    }
  },

  // created() {
  //   this.timelines = require("../../data/timeline.json");
  // }
}
</script>


