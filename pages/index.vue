<template>
  <div>
    <article>
      <h1>News</h1>
      <my-news
        :image="image"
        :title="title"
        :content="content" 
      />
      <section>
        <div class="left column">
          <articles-list />
        </div>
        <div class="right column">
          <posts-list />
        </div>
      </section>
    </article>
    <my-footer />
  </div>
</template>

<script>
// @ is an alias to /src
import MyNews from '@/components/MyNews.vue'
import ArticlesList from '@/components/ArticlesList.vue'
import PostsList from '@/components/PostsList.vue'
import MyFooter from '@/components/MyFooter.vue'
import data from '@/config/data'

export default {
  components: {
    'my-news': MyNews,
    'articles-list': ArticlesList,
    'posts-list': PostsList,
    'my-footer': MyFooter
  },
  data: () => ({
    image: data.home.image,
    title: data.home.title,
    content: data.home.content
  })
}
</script>
