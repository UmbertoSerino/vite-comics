<script>
export default {
  name: 'AppFooter',
  data() {
    return {

    }
  },
}
</script>

<template lang="">
  <footer>
    <section class="footer-top">

    </section>
    <section class="footer-bottom">

    </section>
  </footer>

</template>

<style lang="scss" scoped>
@use '../style/partials/mixins' as*;
@use '../style/partials/variables' as*;

section.footer-top {
  background-image: url(../assets/img/footer-bg.jpg);
  height: 370px;
}

section.footer-bottom {
  background-color: $footer-bt-bg-color;
  height: 110px;
}
</style>