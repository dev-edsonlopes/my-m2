<template>
  <div>
    <Login :logo="logo_src" :alt="alt_name"/>
    <router-view />
  </div>
</template>
<script>
import Login from "./components/Login.vue";
export default {
  name: "App",
  data() {
    return {
      logo_src: "/img/logo.png",
      app_name: "mobs2",
    }
  },
  components: {
    Login,
  },
};
</script>
<style>
* {
  font-family: Helvetica, sans-serif;
  padding: 0;
  margin: 0;
  box-sizing: border-box;
}
</style>
