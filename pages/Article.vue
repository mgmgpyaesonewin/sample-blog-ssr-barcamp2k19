<template>
  <div>
    <article id="post">
      <my-news
        :image="image"
        :title="title"
        :content="content"
      />
    </article>
    <my-footer />
  </div>
</template>

<script>
import MyNews from '@/components/MyNews.vue'
import MyFooter from '@/components/MyFooter.vue'
import data from '@/config/data'

export default {
  components: {
    'my-news': MyNews,
    'my-footer': MyFooter
  },
  computed: {
    image() {
      return data.articles.articles[this.$route.params.id - 1].image
    },
    title() {
      return data.articles.articles[this.$route.params.id - 1].title
    },
    content() {
      return data.articles.articles[this.$route.params.id - 1].content
    }
  }
}
</script>
