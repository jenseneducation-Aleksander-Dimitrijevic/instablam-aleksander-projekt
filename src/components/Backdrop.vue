<template>
  <div class="back-drop" @click="closeAside" :class="{ toggle : isOpen }"></div>
</template>

<script>
import { mapState } from "vuex";
export default {
  name: "Backdrop",
  computed: { ...mapState(["isOpen"]) },
  methods: {
    closeAside() {
      this.$store.commit("TOGGLE_SIDEMENU");
    }
  }
};
</script>

<style lang="scss" scoped>
.back-drop {
  transition: 0.3s;
  &.toggle {
    top: 0;
    right: 0;
    z-index: 1;
    width: 100%;
    height: 100%;
    position: fixed;
    background: rgba(#000, 0.65);
  }
}

@media screen and (min-width: 1440px) {
  .back-drop {
    cursor: pointer;
  }
}
</style>