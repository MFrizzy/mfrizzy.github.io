<template>
  <v-app>
    <v-content>
      <Main />
      <Timeline />
    </v-content>
  </v-app>
</template>

<script>
import Main from "./components/Main";
import Timeline from "./components/Timeline";

export default {
  name: "App",
  components: {
    Main,
    Timeline
  },
  data: () => ({
    //
  })
};
</script>

