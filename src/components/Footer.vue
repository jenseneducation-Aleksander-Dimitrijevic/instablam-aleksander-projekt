<template>
  <footer>
    <button v-if="isActive" class="bell" @click="toggleNotification" title="Blockera aviseringar">
      <i class="far fa-bell"></i>
    </button>
    <button class="bell" v-else title="Tillåt aviseringar" @click="toggleNotification">
      <i class="far fa-bell-slash"></i>
    </button>
    <p>Created by me, Aleksander Dimitrijevic</p>
  </footer>
</template>

<script>
export default {
  name: "footerComponent",
  data() {
    return {
      isActive: false
    };
  },
  methods: {
    toggleNotification() {
      this.isActive = !this.isActive;
    }
  }
};
</script>

<style lang="scss" scoped>
footer {
  padding: 2rem 0;
  margin-top: 2rem;
  text-align: center;
  border-top: 1px solid #eee;

  .bell {
    border: none;
    outline: none;
    font-size: 2rem;
    cursor: pointer;
    background: none;
    transition: 0.3s;
    margin-bottom: 1rem;
  }
}

@media screen and (min-width: 1440px) {
  footer > #bell {
    &:hover {
      transform: scale(1.5);
    }
  }
}
</style>
