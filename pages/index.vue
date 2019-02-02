<template>
  <div class="container has-text-centered">
    <h1 class="title">md2k-spa</h1>
    <h2 class="subtitle">My kryptonian Nuxt.js project</h2>
    <div class="links">
      <a
        href="https://nuxtjs.org/"
        target="_blank"
        class="button--green"
      >Documentation</a>
      <a
        href="https://github.com/nuxt/nuxt.js"
        target="_blank"
        class="button--grey"
      >GitHub</a>
    </div>
  </div>
</template>

<script>
import Logo from "~/components/Logo.vue";

export default {
  components: {
    Logo
  },
  layout: "landing",
  head() {
    return {
      title: "Home"
    };
  }
};
</script>

<style>
</style>
