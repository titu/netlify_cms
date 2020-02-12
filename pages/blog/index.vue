<template>
  <div>
    <ul>
      <li v-for="blog in blogPosts" :key="blog.slug">
        <router-link :to="`/blog/${blog.slug}`">{{blog.title}}</router-link>
      </li>
    </ul>
    <router-view></router-view>
  </div>
</template>
<script>
export default {
  computed: {
    blogPosts () {
      return this.$store.state.blogPosts
    }
  }
}
</script>
