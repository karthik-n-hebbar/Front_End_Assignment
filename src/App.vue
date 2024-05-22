<template>
  <body>
    <sign_in />
    <!-- <popUp v-if="popupTriggers.buttonTriggers" /> -->
  </body>
</template>

<script>
import sign_in from "./components/sign_in.vue";
// import popUp from "./components/popUp.vue";
// import { ref } from "vue";

export default {
  name: "App",
  components: {
    sign_in,
    // popUp,
  },
  // setup() {
  //   const popupTriggers = ref({
  //     buttonTriggers: false,
  //   });

  //   const TogglePopUp = (trigger) => {
  //     popupTriggers.value[trigger] = !popupTriggers.value[trigger];
  //   };
  //   return {
  //     popUp,
  //     popupTriggers,
  //     TogglePopUp,
  //   };
  // },
};
</script>

<style></style>
