<template>
  <Layout>
    <h1>All Blog Posts</h1>
    <p>Wonderful articles on JavaScript and the web.</p>

    <SinglePostCard
      class="posts-list"
      v-for="edge in $page.posts.edges"
      :key="edge.node.uuid"
      :post="edge.node"
    />
  </Layout>
</template>

<page-query>
query{
  posts:allStoryblokEntry{
    edges{
      node{
        name
        full_slug
      	first_published_at(format: "DD-MMM-YYYY")
        uuid
        content
      }
    }
  }
}
</page-query>

<script>
import SinglePostCard from '~/components/SinglePostCard.vue';
export default {
  metaInfo: {
    title: 'Blog'
  },
  components: {
    SinglePostCard
  }
};
</script>
