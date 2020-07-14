<template>
  <div class="body container mx-auto">
    <h1>Blog Posts</h1>
    <ul>
      <div class="grid grid-cols-3 gap-2">
        <li v-for="article of articles" :key="article.slug">
          <NuxtLink
            class="article-link"
            :to="{ name: 'publications-slug', params: { slug: article.slug } }"
          >
            <img class="article-image" :src="article.image" />
            <div class="my-4">
              <h2>{{ article.title }}</h2>
              <div class="text-gray-600">{{ article.description }}</div>
              <div class="mt-4"><author :article="article" /></div>
            </div>
          </NuxtLink>
        </li>
      </div>
    </ul>
  </div>
</template>

<script>
import Author from '~/components/publications/Author'
export default {
  name: 'IndexVue',
  components: { Author },
  async asyncData({ $content, params }) {
    const articles = await $content('publications', params.slug)
      .only(['title', 'description', 'image', 'slug', 'author', 'createdAt'])
      .sortBy('createdAt', 'asc')
      .fetch()

    return {
      articles,
    }
  },
}
</script>

<style scoped>
.article-link {
  @apply text-gray-800;
}

li {
  @apply my-8 px-6 transition duration-500 ease-in-out;
}

li:hover {
  @apply transform scale-105 shadow-lg;
}

.article-image {
  @apply h-48 w-full object-cover;
}
</style>
