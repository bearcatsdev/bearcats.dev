<template>
  <div>
    <div class="container mx-auto">
      <h1>Hello world!</h1>
      <p><nuxt-content :document="hello" /></p>
    </div>
  </div>
</template>

<script>
export default {
  async asyncData({ $content }) {
    const hello = await $content('hello').fetch()

    return {
      hello,
    }
  },
}
</script>

<style></style>
