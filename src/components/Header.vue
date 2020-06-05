<template>
  <div>
    <header>
      <div class="burger-icon" title="open menu" @click="toggleSideMenu">
        <div />
        <div />
        <div />
      </div>
      <Heading headingTitle="Instablam" smallHeading="Where photo editing is made simple." />
    </header>
  </div>
</template>

<script>
import Heading from "@/components/Heading.vue";
export default {
  components: {
    Heading
  },
  methods: {
    toggleSideMenu() {
      this.$store.commit("TOGGLE_SIDEMENU");
    }
  }
};
</script>

<style lang="scss" scoped>
header {
  width: 100%;
  display: flex;
  flex-flow: column;
  align-items: center;
}

.burger-icon {
  padding: 20px;
  cursor: pointer;
  margin-left: auto;
  div {
    width: 25px;
    height: 1px;
    margin: 6px 0;
    background: #000;
  }
}
</style>