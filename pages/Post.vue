<template>
  <article id="post">
    <my-news
      :image="image"
      :title="title"
      :content="content"
    />
  </article>
</template>

<script>
import MyNews from '@/components/MyNews.vue'
import data from '@/config/data'

export default {
  components: {
    'my-news': MyNews
  },
  computed: {
    image() {
      return data.posts.posts[this.$route.params.id - 1].image
    },
    title() {
      return data.posts.posts[this.$route.params.id - 1].title
    },
    content() {
      return data.posts.posts[this.$route.params.id - 1].content
    }
  }
}
</script>
