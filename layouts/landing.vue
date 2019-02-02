<template>
  <section class="hero is-fullheight">
    <div class="hero-head">
      <v-navbar/>
    </div>
    <div class="hero-body">
      <nuxt/>
    </div>
    <div class="hero-foot">
      <v-footer/>
    </div>
  </section>
</template>

<script>
import VNavbar from "@/components/VNavbar";
import VFooter from "@/components/VFooter";

export default {
  name: "LayoutLanding",
  components: { VNavbar, VFooter }
};
</script>
