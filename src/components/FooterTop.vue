<script>
export default {
  data() {
    return {
      sectionsLists: {
        'dc-comics': [
          'characters',
          'comics',
          'movies',
          'TV',
          'games',
          'videos',
          'news'],
        shop: [
          'shop DC',
          'shop DC collectibles'],
        DC: [
          'terms of use',
          'privacy policy (new)',
          'ad choices',
          'advertising',
          'subscriptions',
          'talent workshops',
          'CPSC certificates',
          'ratings',
          'shop help',
          'contact us'
        ],
        sites: [
          'DC',
          'MAD magazine',
          'DC kids',
          'DC universe',
          'DC power visa'
        ]
      }
    }
  },
  methods: {
    // Funzione per avere la prima lettera della parola maiuscola
    capitalizeArray (wordsArray) {
      let capitalizedWordsArray = [];
      for (let i = 0; i < wordsArray.length; i++) {
        const word = wordsArray[i];
        const capitalizedFirstLetter = word[0].toUpperCase();
        const capitalizedWord = capitalizedFirstLetter + word.slice(1);
        capitalizedWordsArray.push(capitalizedWord);
      }
      return capitalizedWordsArray;
    },
  },
  computed: {
    sectionsListsProp () {return Object.keys(this.sectionsLists)},
  }
}
</script>

<template>
  <div class="footer-top">
    <div class="container-lg">
      <section class="dc-comics" v-for="prop in sectionsListsProp">
        <h3>{{ capitalizeArray([prop])[0] }}</h3>
        <ul>
          <li v-for="li in capitalizeArray(sectionsLists[prop])"><a href="#">{{ li }}</a></li>
        </ul>
      </section>
    </div>
  </div>
</template>

<style lang="scss" scoped>
  @use '../styles/general.scss' as *;

  /* Custom properties */
  $footer-top-h: 360px;

  .footer-top {
    height: $footer-top-h;

    background-image: url(../assets/img/footer-bg.jpg);

    .container-lg {
      height: 100%;

      display: flex;
      flex-direction: column;
      flex-wrap: wrap;
      align-content: start;
      gap: 20px;

    }

    section {
      width: 15%;
      padding: 10px 0;
      font-size: 0.8rem;

      h3 {
        color: #fff;
        font-size: 1.3rem;
        font-weight: 500;
      }
      
      a {
        color: #ccc;
      }
    };
  }
</style>