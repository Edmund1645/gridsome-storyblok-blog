<template>
  <Layout>
    <h1>Hello!!</h1>

    <p>Welcome to my Awesome Blog where I write about web technologies and my journey as a software developer</p>
    <p>
      <g-link to="/blog">Check out my articles here</g-link>
    </p>
  </Layout>
</template>

<script>
export default {
  metaInfo: {
    title: 'Home'
  }
};
</script>

<style>
.home-links a {
  margin-right: 1rem;
}
</style>
