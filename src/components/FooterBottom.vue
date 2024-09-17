<script>
export default {
  data() {
    return {
      socialLinks: [
        '<i class="bi bi-facebook"></i>',
        '<i class="bi bi-twitter"></i>',
        '<i class="bi bi-youtube"></i>',
        '<i class="bi bi-pinterest"></i>',
        '<i class="bi bi-geo-alt-fill"></i>',
      ]
    }
  }
}
</script>

<template>
  <div class="footer-bottom">
    <div class="container-lg">
      <div class="button-box">
        <button id="sign-up-btn">
          SIGN-UP NOW
        </button>
      </div>
      <section id="social">
        <h3>
          FOLLOW US
        </h3>
        <ul id="social-link" v-for="link in socialLinks">
          <li><a href="#" v-html="link"></a></li>
        </ul>
      </section>
    </div>
  </div>
</template>

<style lang="scss" scoped>
  @use '../styles/general.scss' as general-var;
  @use 'bootstrap-icons/font/bootstrap-icons.css' as *;
  
  /* Custom properties */
  $a-radius: 30px;

  .footer-bottom {
    height: 100px;
    color: #333;
    background-color: currentColor;
  }

  .container-lg {
    height: 100%;

    display: flex;
    justify-content: space-between;
    align-items: center;
  }

  #sign-up-btn {
    padding: 10px 14px;
    color: #fff;
    border: 3px solid general-var.$base-color;
    background-color: transparent;
    transition: background-color 2s;

    font-family: 'Opens sans condensed', sans-serif;

    &:hover {
      background-color: general-var.$base-color;
      border-color: #fff;
    }
  }

  #social,
  #social-link {
    display: flex;
  }

  #social {
    h3 {
      margin-right: 20px;
      color: general-var.$base-color;
    }

    #social-link a {
      color: currentColor;
      background-color: #888;
      font-size: 1.2rem;
      display: inline-block;
      margin-right: 5px;
      width: $a-radius;
      height: $a-radius;
      border-radius: 50%;
      text-align: center;
      line-height: $a-radius;
    }
  }
</style>