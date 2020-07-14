<template>
  <div class="navbar">
    <div class="navbar-content container">
      <div class="branding">
        <nuxt-link to="/"
          ><img src="@/assets/img/bearcats.svg" class="h-full"
        /></nuxt-link>
      </div>
      <nav>
        <ul>
          <li>
            <nuxt-link class="nuxt-link" active-class="active" exact to="/"
              >Home</nuxt-link
            >
          </li>
          <li>
            <nuxt-link class="nuxt-link" active-class="active" to="/innovations"
              >Innovations</nuxt-link
            >
          </li>
          <li>
            <nuxt-link
              class="nuxt-link"
              active-class="active"
              to="/publications"
              >Publications</nuxt-link
            >
          </li>
        </ul>
      </nav>
    </div>
  </div>
</template>

<script>
export default {
  name: 'TheNav',
}
</script>

<style scoped>
.navbar {
  @apply w-screen bg-white fixed z-10;
}
.navbar-content {
  @apply py-4 flex justify-between h-navbar items-center mx-auto;
}
nav > ul > li {
  @apply inline float-left px-4;
}
.nuxt-link {
  @apply no-underline text-gray-600 flex flex-col items-center uppercase font-display transition duration-500 ease-in-out;
}
.nuxt-link:hover {
  @apply text-primary;
}
.active {
  @apply text-primary;
}
.branding {
  @apply h-full py-2;
}
</style>
