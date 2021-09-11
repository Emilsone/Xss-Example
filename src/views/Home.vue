<template>
  <div class="home">
    <img alt="Vue logo" src="../assets/logo.png" />
    <XssPage />
  </div>
</template>

<script>
// @ is an alias to /src
import XssPage from "@/components/XssPage.vue";

export default {
  name: "Home",
  components: {
    XssPage,
  },
};
</script>

<style>
.dummy-text {
  font-size: 25px;
}
</style>
