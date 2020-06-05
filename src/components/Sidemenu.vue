<template>
  <aside :class="{ toggle : isOpen }">
    <span class="close-btn" @click="closeAside">&times;</span>
    <h1>Menu</h1>
    <ul>
      <li>
        <router-link
          to="/"
          @click.native="getMedia(); closeAside();"
          @click="closeAside"
        >Start camera</router-link>
      </li>
    </ul>
  </aside>
</template>

<script>
import { mapState } from "vuex";
export default {
  name: "Sidemenu",
  computed: { ...mapState(["isOpen"]) },
  methods: {
    closeAside() {
      this.$store.commit("TOGGLE_SIDEMENU");
    },
    getMedia() {
      this.$root.$emit("start-camera");
    }
  }
};
</script>

<style lang="scss" scoped>
aside {
  top: 0;
  right: 0;
  width: 80%;
  z-index: 2;
  height: 100%;
  position: fixed;
  max-width: 300px;
  transition: 0.3s;
  text-align: center;
  overflow-x: hidden;
  background: #fff;
  transform: translateX(100%);

  span.close-btn {
    top: 0;
    right: 1rem;
    cursor: pointer;
    font-size: 3rem;
    position: absolute;
  }

  h1 {
    margin-top: 4rem;
  }

  ul {
    margin: 2rem 0;

    a {
      color: #222;
      display: block;
      font-size: 1.2rem;
    }
  }

  &.toggle {
    transform: translateX(0);
  }
}
</style>