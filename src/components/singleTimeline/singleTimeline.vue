<template>
  <div class="single-component">
    <div class="single-component__name">{{fullName}}</div>
    <div class="single-component__about">{{timeline.about}}</div>
    <div class="single-component__registered">{{timeline.registered}}</div>
    <ul class="tag__list">
      <li class="tag__item" v-for="tag in cover" :key="tag.id">
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
  
  computed: {
    fullName() {
      return this.timeline.name.first + " " + this.timeline.name.last;
    },
     
    cover() {
      return this.timeline.tags.splice(', '); 
    },
  
    sortedByData: function () {
      let formData = Date.parse(this.timeline.registered)
      return  formData
    }
  }
}
</script>

<style lang="postcss" scoped src="./singleTimeline.pcss"></style>