<template>
  <v-app>
    <toolbar />
    <v-content style="background-color: white">
      <router-view />
    </v-content>
    <footer />
  </v-app>
</template>

<script>
import Toolbar from "./components/Toolbar";
import Footer from "./components/Footer";

export default {
  name: "App",
  components: {
    Toolbar,
    /* eslint-disable vue/no-unused-components */
    Footer
  },

  data: () => ({
    //
  })
};
</script>
