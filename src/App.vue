<template>
  <div id="app">
    <app-registration></app-registration>
    <app-registrations></app-registrations>
  </div>
</template>

<script>
import AppRegistration from "./components/AppRegistration.vue";
import AppRegistrations from "./components/AppRegistrations.vue";

export default {
  components: {
    appRegistration: AppRegistration,
    appRegistrations: AppRegistrations,
  },
};
</script>

<style>
#app {
  font-family: "Avenir", Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>