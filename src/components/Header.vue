<template>
  <div>
    <header>
      <Heading headingTitle="Instablam" smallHeading="Where photo editing is made simple." />
    </header>
  </div>
</template>

<script>
import Heading from "@/components/Heading.vue";
export default {
  components: {
    Heading
  }
};
</script>

<style lang="scss" scoped>
header {
  width: 100%;
  display: flex;
  justify-content: center;
}
</style>