<template>
  <div class="home">
    <h1>Home</h1>
    <div v-if="error">{{ error }}</div>
    <div v-if="posts.length">
      <PostList :posts="posts" />
    </div>
    <div v-else>Loading...</div>
  </div>
</template>

<script>
import PostList from '../components/PostList.vue'
import getPost from '../composable/getPost.js'

export default {
  name: 'Home',
  components: { PostList, getPost },
  setup() {
    
    return { posts, error }
  }
}
</script>