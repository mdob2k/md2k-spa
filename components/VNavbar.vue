<template>
  <nav
    class="navbar"
    role="navigation"
    aria-label="main navigation"
  >
    <div class="navbar-brand">
      <nuxt-link
        class="navbar-item has-text-weight-bold"
        to="/"
        exact
      >md2k</nuxt-link>

      <a
        :class="[{'is-active': isActive}, 'navbar-burger']"
        role="button"
        aria-label="menu"
        aria-expanded="false"
        data-target="navMenu"
        @click="isActive = !isActive"
      >
        <span aria-hidden="true"/>
        <span aria-hidden="true"/>
        <span aria-hidden="true"/>
      </a>
    </div>
    <div
      id="navMenu"
      :class="[{'is-active': isActive}, 'navbar-menu']"
    >
      <div class="navbar-start"/>
      <div class="navbar-end">
        <nuxt-link
          to="/demos"
          class="navbar-item is-tab"
        >Demos</nuxt-link>
        <nuxt-link
          to="/about"
          class="navbar-item is-tab"
        >About</nuxt-link>
      </div>
    </div>
  </nav>
</template>

<script>
export default {
  name: "VNavbar",
  data: () => {
    return {
      isActive: false
    };
  },
  watch: {
    $route(to, from) {
      this.isActive = false;
    }
  }
};
</script>
