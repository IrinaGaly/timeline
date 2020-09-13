<template>
  <div class="single-component">
    <div class="full-name">{{fullName}}</div>
    <div class="about">{{timeline.about}}</div>
    <div class="registered">{{timeline.registered}}</div>
    <ul class="tag__list">
      <li class="tag__item" v-for="tag in cover">
        <tag :tag="tag">{{tag}}</tag>
      </li>
    </ul> 
  </div>
</template>

<script>
import tag from "../tag/tag"

export default {
  components: {tag},
  props: {
    timeline: {
      type: Object,
      default: () => {}
    }
  },

  data() {
    return {
      timelines: {
        id: "",
        name: {
          first: "",
          last: ""
        },
        about: "",
        registered: '',
        tags: []
      }
    }
  },
  computed: {
    fullName() {
      return this.timeline.name.first + " " + this.timeline.name.last;
    },
     
    cover() {
      return this.timeline.tags.splice(', '); 
    },

    myData() {
      return Date.parse(this.timeline.registered);
      
    }, 
    sortbydate() {
      
    }
}
</script>


<style lang="postcss" scoped src="./singleTimeline.pcss"></style>