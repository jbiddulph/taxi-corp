<template>
  <div id="app">
    <NavMenu />
    <router-view />
  </div>
</template>

<script>
import NavMenu from "@/components/NavMenu.vue";
export default {
  name: "App",
  components: {
    NavMenu,
  },
};
</script>
