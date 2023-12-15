<script>
import HeroesCard from './HeroesCard.vue';

export default {
  name: 'AppMain',
  data() {
    return {};
  },
  components: { HeroesCard }
}
</script>

<template>
  <main class="main-container">
    <section class="container-jumbotron">
      <div class="current-text">
        <p class="current">Current Series</p>
      </div>
    </section>
    <HeroesCard />
  </main>
</template>

<style lang="scss" scoped>
@use '../style/partials/mixins' as*;
@use '../style/partials/variables' as*;

main.main-container {
  background-color: $main-bd-color;
  width: 100%;
  color: $main-text-color;


  section.container-jumbotron {
    height: 100%;
    height: 400px;
    @include flex(row, start, center);
    background-image: url(../assets/img/jumbotron.jpg);
    position: relative;

    div.current-text {
      @include container(width, margin);

      p.current {
        background-color: $main-bg-current;
        padding: .5rem;
        position: absolute;
        bottom: 0;
        transform: translate(0%, 50%);
      }

    }
  }
}
</style>