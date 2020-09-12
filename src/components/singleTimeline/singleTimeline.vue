<template>
  <div class="single-component">
    <div class="name">{{timeline.name}}</div>
    <div class="about">{{timeline.about}}</div>
    <div class="registered">{{timeline.registered}}</div>
    <div class="tags">{{timeline.tags}}</div>
  </div>
</template>

<script>


export default {
 props: {
   timeline: {
     type: Object,
     default: () => {}
   }
 },

  data() {
    return {
      timelines,
      timeline: {
        id: "",
        name: "",
        about: "",
        registered: "",
        tags: ""
      }
    }
  }
  
}
</script>