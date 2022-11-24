<template>
  <div class="home">
    <h1>Home</h1>
    <PostList v-if="showPosts" :posts="posts" />
    <button @click="showPosts = !showPosts">toggle posts</button>
  </div>
</template>

<script>
import PostList from '../components/PostList.vue'
import { ref } from 'vue'

export default {
  name: 'Home',
  components: { PostList },
  setup() {
    const posts = ref([
      { title: 'Welcome to the blog', body: 'Lorem ipsum dolor sit amet, consectetur adipiscing elit. Integer mi ligula, tempus a luctus eu, condimentum ac metus. Vestibulum justo mi, ultrices sit amet enim eget, fringilla feugiat erat. Phasellus varius purus vitae volutpat pulvinar. Donec at elit hendrerit, eleifend erat id, tristique ante. Maecenas volutpat, arcu in pretium malesuada, sem massa maximus ante, et pulvinar nunc dolor et enim. Curabitur tincidunt malesuada rhoncus. Nam elementum ultrices blandit. Fusce congue nisi mattis, finibus diam a, posuere ante. Nunc neque est, vulputate nec pulvinar ac, euismod in nisl. Morbi a ligula sed urna blandit ullamcorper et sed risus. Vivamus et est varius, faucibus nibh at, ornare erat. Suspendisse rhoncus tincidunt mauris, sed mollis eros sagittis eu.', id: 1 },
      { title: 'top 5 CSS tips', body: 'Lorem ipsum dolor sit amet, consectetur adipiscing elit. Integer mi ligula, tempus a luctus eu, condimentum ac metus. Vestibulum justo mi, ultrices sit amet enim eget, fringilla feugiat erat. Phasellus varius purus vitae volutpat pulvinar. Donec at elit hendrerit, eleifend erat id, tristique ante. Maecenas volutpat, arcu in pretium malesuada, sem massa maximus ante, et pulvinar nunc dolor et enim. Curabitur tincidunt malesuada rhoncus. Nam elementum ultrices blandit. Fusce congue nisi mattis, finibus diam a, posuere ante. Nunc neque est, vulputate nec pulvinar ac, euismod in nisl. Morbi a ligula sed urna blandit ullamcorper et sed risus. Vivamus et est varius, faucibus nibh at, ornare erat. Suspendisse rhoncus tincidunt mauris, sed mollis eros sagittis eu.', id: 2 },
    ])
    const showPosts = ref(true)
    
    return { posts, showPosts }
  }
}
</script>
