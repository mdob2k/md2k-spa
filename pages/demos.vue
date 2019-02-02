<template>
  <div class="page-demos">
    <section class="hero">
      <div class="hero-body">
        <div class="container">
          <h1 class="title">Demos</h1>
          <button
            v-for="view in views"
            :key="view.id"
            class="button"
            @click="currentView = view.name"
          >{{ view.name }}</button>
        </div>
      </div>
    </section>

    <section class="section demo-components">
      <div class="container">
        <component :is="currentView"/>
      </div>
    </section>
  </div>
</template>

<script>
import Demo01 from "@/components/Demo01";
import Demo02 from "@/components/Demo02";
export default {
  name: "Demos",
  components: { Demo01, Demo02 },
  head() {
    return {
      title: "Demos"
    };
  },
  data: () => {
    return {
      views: [{ id: 0, name: "Demo01" }, { id: 1, name: "Demo02" }],
      currentView: false
    };
  }
};
</script>
