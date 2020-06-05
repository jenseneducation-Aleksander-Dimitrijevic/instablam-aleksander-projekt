<template>
  <div id="app">
    <Header />
    <Backdrop />
    <router-view />
    <Sidemenu />
    <Footer />
  </div>
</template>

<script>
import Header from "@/components/Header.vue";
import Footer from "@/components/Footer.vue";
import Sidemenu from "@/components/Sidemenu.vue";
import Backdrop from "@/components/Backdrop.vue";
export default {
  name: "app",
  components: {
    Header,
    Footer,
    Sidemenu,
    Backdrop
  }
};
</script>

<style lang="scss">
@import url("https://fonts.googleapis.com/css2?family=Open+Sans:wght@300&display=swap");
* {
  padding: 0;
  margin: 0;
  box-sizing: border-box;
}
body,
input,
::placeholder {
  font-family: "Open Sans", sans-serif;
}
#app {
  width: 100%;
  height: 100vh;
  display: flex;
  flex-flow: column;
  justify-content: space-between;
}
</style>
