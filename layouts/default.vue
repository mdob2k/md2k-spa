<template>
  <div class="layout-default">
    <v-navbar/>
    <nuxt/>
    <v-footer/>
  </div>
</template>

<script>
import VNavbar from "@/components/VNavbar";
import VFooter from "@/components/VFooter";

export default {
  name: "LayoutDefault",
  components: {
    VNavbar,
    VFooter
  }
};
</script>
