<template>
  <div class="post">
    <h2>
      <g-link :to="post.full_slug">{{ post.name }}</g-link>
    </h2>
    <p>{{post.content.description}}</p>
    <p>
      <small>
        <em>{{post.first_published_at}}</em>
      </small>
    </p>
  </div>
</template>

<script>
export default {
  props: ['post']
};
</script>

<style scoped>
.post {
  border-bottom: 1px dashed var(--border-color);
  margin-top: 40px;
}
</style>