<template>
  <div id="app">
    <GoogleMap />
    <Wasyoku />
  </div>
</template>

<script>
import Wasyoku from "./components/EastAsia/Wasyoku.vue"
import GoogleMap from "./components/Map.vue"
export default {
  name: "App",
  components: {
    Wasyoku,
    GoogleMap,
  },
}
</script>

<style></style>
