<template>
  <div class="container has-text-centered">
    <h1 class="title">md2k-spa</h1>
    <h2 class="subtitle">My kryptonian Nuxt.js project</h2>
    <logo/>
    <div class="links">
      <a
        class="button--green"
        href="https://nuxtjs.org/"
        target="_blank"
      >Documentation</a>
      <a
        class="button--grey"
        href="https://github.com/nuxt/nuxt.js"
        target="_blank"
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
