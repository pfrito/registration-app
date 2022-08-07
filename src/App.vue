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
  data() {
    return {
      registrations: [],
      users: [
        { id: 1, name: "Max", registered: false },
        { id: 2, name: "Anna", registered: false },
        { id: 3, name: "Chris", registered: false },
        { id: 4, name: "Sven", registered: false },
      ],
    };
  },
  computed: {
    unregisteredUsers() {
      return this.users.filter((user) => {
        return !user.registered;
      });
    },
  },
  methods: {
    userUnregistered(registration) {
      const user = this.users.find((user) => {
        return user.id == registration.userId;
      });
      user.registered = false;
      this.registrations.splice(this.registrations.indexOf(registration), 1);
    },
  },
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