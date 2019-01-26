<template>
  <div>
    <h4 class="list-title">
      Archived Posts
    </h4>
    <ul class="vertical-list">
      <li
        v-for="(post, index) in posts"
        :key="index"
        class="list-item"
      >
        <router-link
          :to="`post/${post.id}`"
          class="post-link"
        >
          {{ post.title }}
        </router-link>
      </li>
      <!-- <li class="list-item"><a href="pages/article-missing.html" class="post-link">Non-existent article</a></li> -->
    </ul>
  </div>
</template>

<script>
import data from '@/config/data'

export default {
  data: () => ({
    posts: data.posts.posts
  })
}
</script>
