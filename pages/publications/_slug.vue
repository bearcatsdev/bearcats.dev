<template>
  <article>
    <img class="article-image" :src="article.image" :alt="article.alt" />
    <div class="body container mx-auto">
      <h1>{{ article.title }}</h1>
      <div class="text-gray-600">{{ article.description }}</div>
      <div class="my-4"><author :article="article" /></div>
      <nuxt-content :document="article" />
    </div>
  </article>
</template>

<script>
import Author from '~/components/publications/Author'
export default {
  name: 'Slug',
  components: { Author },
  async asyncData({ $content, params }) {
    const article = await $content('publications', params.slug).fetch()

    return { article }
  },
}
</script>

<style scoped>
.article-image {
  @apply w-full object-cover;
  height: 30rem;
}
</style>
