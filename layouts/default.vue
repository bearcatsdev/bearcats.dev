<template>
  <div>
    <the-nav />
    <Nuxt class="pt-navbar" />
    <the-footer />
  </div>
</template>

<style></style>
<script>
import TheNav from '~/components/TheNav'
import TheFooter from '~/components/TheFooter'
export default {
  components: { TheFooter, TheNav },
}
</script>
