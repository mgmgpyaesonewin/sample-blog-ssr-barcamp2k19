<template>
  <div>
    <h4 class="list-title">
      Trending Articles
    </h4>
    <ul class="vertical-list">
      <li
        v-for="(article, index) in articles"
        :key="index"
        class="list-item"
      >
        <router-link
          :to="`article/${article.id}`"
          class="post-link"
        >
          {{ article.title }}
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
    articles: data.articles.articles
  })
}
</script>
