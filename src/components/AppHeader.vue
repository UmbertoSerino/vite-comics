<script>
export default {
  name: 'AppHeader',
  data() {
    return {
      navBar: [
        'Characters',
        'Comics',
        'Movies',
        'TV',
        'Games',
        'Collectibles',
        'Videos',
        'Fans',
        'News',
        'Shop'
      ]
    }
  },
}
</script>

<template lang="">
  <header class="header-top">
    <section class="container">
      <div class=logo>
        <img src="../assets/img/dc-logo.png" alt="">
      </div>
      <nav>
        <ul>
          <li v-for="(item, index) in navBar" :key="index">
            {{ item }}
          </li>
        </ul>

      </nav>
    </section>

  </header>
</template>

<style lang="scss" scoped>
@use '../style/partials/mixins' as*;
@use '../style/partials/variables' as*;

header.header-top {
  background-color: $header-bg-color ;
  width: 100%;
  height: 120px;

  section.container {
    height: 100%;
    @include flex(row, space-between, center);
    @include container(width, margin);

    img {
      height: 85px;
    }
  }

  ul {
    list-style-type: none;
    @include flex(row, center, center);
    flex-wrap: wrap;

    li {
      padding: .7rem;
      text-transform: uppercase;
      font-size: .65rem;
      font-family: sans-serif;
      font-weight: bolder;

      &.active {
        border-bottom: 5px solid black;
        color: $header-text-color;
      }

      &:hover {
        color: $header-text-color;
        cursor: pointer;
      }

    }
  }
}
</style>