<script>
export default {
  name: 'AppFooter',
  data() {
    return {
      dcComicsList: [
        'Characters', 'Comics', 'Moveies', 'Tv', 'Games', 'Videos', 'News'
      ],
      shopList: [
        'Shop DC', 'Shop DC Cpòòactibles'
      ],
      dcList: ['Terms Of USE', 'Privacy policy (New)', 'Ad Choices', 'Advertising', 'Jobs', 'Sibsciptions', 'Talent Workshops', 'CPSC Certificates', 'Ratings', 'Shop Help', 'Contact US'],
      sitesList: ['DC', 'MAD Magazine', 'DC Kids', 'DC Universe', 'DC Power Visa']
    }
  },
}
</script>

<template lang="">
<footer>
  <div class="big-container-footer">
    <section class="footer-top">
      <div class="container-list">
        <div>
          <ul>
            <h1>dc comics</h1>
            <li v-for=" itemsDCComics in dcComicsList">
              {{ itemsDCComics }}
            </li>
          </ul>
          <ul>
            <h1>
              Shop
            </h1>
            <li v-for="itemsShopList in shopList">
              {{ itemsShopList }}
            </li>
          </ul>
        </div>
        <div>
          <ul>
            <h1>
              dc
            </h1>
            <li v-for="itemsDCList in dcList">
              {{ itemsDCList }}
            </li>
          </ul>
        </div>
        <div>
          <ul>
            <h1>Sites</h1>
            <li v-for="itemsSitesList in sitesList">
              {{ itemsSitesList }}
            </li>
          </ul>

        </div>
      </div>
      <div>
        <img src="../assets/img/dc-logo-bg.png" alt="">
      </div>
    </section>
  </div>
  <section class="footer-bottom">
    <div class="container-footer-bottom">
      <div>
        <button>Sign-Up Now!</button>
      </div>
      <div class="container-icon">
        <p class="follow">Follow us</p>
        <img src="../assets/img/footer-facebook.png" alt="pictures logo facebook">
        <img src="../assets/img/footer-twitter.png" alt="picture logo twitter">
        <img src="../assets/img/footer-youtube.png" alt="picture logo youtube">
        <img src="../assets/img/footer-pinterest.png" alt="picture logo pinterest">
        <img src="../assets/img/footer-periscope.png" alt="picture logo periscope">
      </div>
    </div>

  </section>
      
</footer>

</template>

<style lang="scss" scoped>
@use '../style/partials/mixins' as*;
@use '../style/partials/variables' as*;

div.big-container-footer {
  background-image: url(../assets/img/footer-bg.jpg);
  width: 100%;

}

section.footer-top {
  height: 370px;
  @include container(width, margin);


  color: $footer-text-color;
  @include flex (row, space-between, center);
  overflow: hidden;


  div.container-list {
    display: flex;
    flex-direction: column;
    flex-wrap: wrap;
    height: 100%;
    width: 65%;


    ul {
      h1 {
        text-transform: uppercase;
        padding: 1.5rem 0;
      }

      li {
        color: $footer-text-list-color;
        list-style-type: none;
        font-size: .7rem;
        margin-bottom: .34rem;
      }
    }

  }
}

section.footer-bottom {
  background-color: $footer-bt-bg-color;
  height: 110px;
  @include flex(row, space-between, center);

  div.container-footer-bottom {
    @include container(width, margin);
    @include flex(row, space-between, center);

    button {
      background-color: $footer-bt-bg-color;
      color: $footer-text-color;
      border: 2px solid $footer-border-color;
      padding: .5rem .7rem;
      text-transform: uppercase;
    }

    div.container-icon {
      display: flex;
      flex-direction: row;
      align-items: center;

      p.follow {
        margin-right: 10px;
        color: $footer-bottom-text;
        text-transform: uppercase;
        font-weight: bold;
      }

      img {
        margin-right: .8rem;
      }
    }

  }
}
</style>