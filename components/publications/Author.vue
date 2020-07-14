<template>
  <div class="flex items-center">
    <img class="profile-picture" :src="article.author.image" />
    <div class="ml-4">
      <div>{{ article.author.name }}</div>
      <div class="text-gray-600">
        {{ formatDate(article.createdAt) }}
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'Author',
  props: {
    article: {
      type: Object,
      required: true,
    },
  },
  methods: {
    formatDate(date) {
      const options = { year: 'numeric', month: 'long', day: 'numeric' }
      return new Date(date).toLocaleDateString('en', options)
    },
  },
}
</script>

<style scoped>
.profile-picture {
  @apply rounded-full w-12 h-12 object-cover;
}
</style>
