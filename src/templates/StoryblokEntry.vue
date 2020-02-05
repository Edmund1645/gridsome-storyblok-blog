<template>
  <Layout>
    <h1 class="title">{{$page.post.name}}</h1>
    <p class="date">
      Published on.
      <em>{{$page.post.first_published_at}}</em>
    </p>
    <hr />
    <Richtext
      v-if="$page.post.content.body"
      :key="$page.post.content._uid"
      :text="$page.post.content.body"
    />
  </Layout>
</template>

<page-query>
query StoryblokEntry ($id: ID) {
  post:storyblokEntry (id: $id) {
    id
    slug
    name
    content
    first_published_at(format: "DD-MMM-YYYY")
  }
}
</page-query>

<script>
import Richtext from '~/components/Richtext.vue';
export default {
  components: {
    Richtext
  }
};
</script>

<style scoped>
.title {
  text-align: center;
}
.date {
  opacity: 0.5;
  text-align: center;
}
</style> 