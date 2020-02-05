<template>
  <div>
    <div v-html="richtext"></div>
  </div>
</template>

<script>
export default {
  name: 'ContentField',
  props: ['text'],
  computed: {
    richtext() {
      return this.text ? this.$storyapi.richTextResolver.render(this.text) : "<p>There's no text to render :/</p>";
    }
  }
};
</script>

<style scoped>
</style>