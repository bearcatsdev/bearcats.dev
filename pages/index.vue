<template>
  <div>
    <div class="hero" />
    <!-- Hey there -->
    <div class="bg-gray-100">
      <div class="body container">
        <div class="split-half">
          <div class="content">
            <h1>Hey there!</h1>
            <p class="text-lg">
              We are a team of five tech enthusiasts from the Generation-22
              Mobile Application and Technology program at BINUS University and
              we're excited to help the society using what we're good at,
              technology.
            </p>
            <div>Read more</div>
          </div>
          <img
            class="ml-12 rounded-lg"
            src="../assets/img/who-we-are.jpg"
            alt="Bearcats members"
            style="height: 300px;"
          />
        </div>
      </div>
    </div>

    <!-- Our works -->
    <div class="body container">
      <div class="text-center">
        <h1>Our works</h1>
        <p>These are some of the project that we did or involved with.</p>
      </div>

      <!-- Adab -->
      <div class="split-half">
        <div class="content">
          <img class="logo" src="../assets/img/adab-logo.png" alt="Adab logo" />
          <h2>Adab</h2>
          <p class="text-lg">
            Ayo Dengar Ayo Bicara (ADAB) is an app to help deaf and mute
            students at BINUS University by providing access to real-time speech
            transcription service allowing them to better understand the
            lecturers.
          </p>
          <div>Read more</div>
        </div>
        <div class="content">
          <img
            class="w-full ml-12 rounded-lg"
            src="../assets/img/adab.png"
            alt="Adab"
          />
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  components: {},
}
</script>

<style>
.hero {
  height: 75vh;
  background: url('../assets/img/hero-bearcats.jpeg') no-repeat;
  background-size: cover;
}
.body {
  @apply mx-auto py-12;
}
p {
  @apply my-4;
}
.split-half {
  @apply flex justify-between items-center py-6;
}
.split-half > .content {
  @apply w-full;
}
.split-half > .content > .logo {
  @apply h-16 pb-4;
}
</style>
