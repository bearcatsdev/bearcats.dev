<template>
  <div>
    <div class="bg-gray-100">
      <div class="body container">
        <div class="text-lg">
          <nuxt-content :document="innovations" />
        </div>
      </div>
    </div>
    <div>
      <div class="body container">
        <!-- Adab -->
        <div class="split-half">
          <div class="content">
            <img
              class="logo"
              src="@/assets/img/adab-logo.png"
              alt="Adab logo"
            />
            <h2>Adab</h2>
            <p class="text-lg">
              Ayo Dengar Ayo Bicara (ADAB) is an app to help deaf and mute
              students at BINUS University by providing access to real-time
              speech transcription service allowing them to better understand
              the lecturers.
            </p>
            <div>Read more</div>
          </div>
          <div class="content">
            <img
              class="w-full ml-12 rounded-lg"
              src="@/assets/img/adab.png"
              alt="Adab"
            />
          </div>
        </div>

        <!-- Tamago -->
        <div class="split-half">
          <div class="content">
            <img
              class="logo"
              src="@/assets/img/tamago-logo.png"
              alt="Adab logo"
            />
            <h2>Tamago</h2>
            <p class="text-lg">
              Tamago is a digital penny bank app, designed for young parents to
              teach their kids how to save money in a fun and interactive way.
            </p>
            <div>Read more</div>
          </div>
          <div class="content">
            <img
              class="w-full ml-12 rounded-lg"
              src="@/assets/img/tamago.png"
              alt="Tamago"
            />
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'IndexVue',
  async asyncData({ $content }) {
    const innovations = await $content('innovations').fetch()

    return {
      innovations,
    }
  },
}
</script>

<style scoped></style>
