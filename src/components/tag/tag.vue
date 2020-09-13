<template>
  <div class="tag">{{tag}}</div>
</template>

<script>
export default {
  props: {
    tag: {
      type: String
    }
  }
}
</script>

<style lang="postcss" scoped src="./tag.pcss"></style>