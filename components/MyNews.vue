<template>
  <section>
    <div class="img-container left column">
      <img :src="image" alt="A person reading the business section of a newspaper">
    </div>
    <div class="right column">
      <h2 class="headline">
        {{ title }}
      </h2>
      <p class="content">
        {{ content }}
      </p>
    </div>
  </section>
</template>

<script>
export default {
  props: {
    image: {
      type: String,
      default: ''
    },
    title: {
      type: String,
      default: ''
    },
    content: {
      type: String,
      default: ''
    }
  }
}
</script>
