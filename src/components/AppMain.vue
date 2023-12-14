<script>
export default {
  name: 'AppMain',
  data() {
    return {

    }
  },
}
</script>

<template lang="">
  <main class="main-container">
    <section class="container">
      <h1>
        --&triangleright; Content goes here &triangleleft;--
      </h1>

    </section>
  </main>

</template>

<style lang="scss" scoped>
@use '../style/partials/mixins' as*;
@use '../style/partials/variables' as*;

main.main-container {
  background-color: $main-bd-color;
  width: 100%;
  height: 100px;
  color: $main-text-color;


  section.container {
    height: 100%;
    width: 65%;
    margin: 0 auto;
    @include flex(row, start, center);

    h1 {
      font-size: 1.7rem;
      font-family: sans-serif;

    }
  }
}
</style>