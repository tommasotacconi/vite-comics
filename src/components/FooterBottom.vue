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
  @use '../styles/general.scss' as *;
  @use 'bootstrap-icons/font/bootstrap-icons.css' as *;
  
  /* Custom properties */
  $a-radius: 30px;

  .footer-bottom {
    height: 100px;
    background-color: #666;
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
    border: 4px solid $base-color;
    background-color: transparent;

    &:hover {
      background-color: $base-color;
      border-color: #fff;
      transition: background-color 20s;
      transition: border-color 1s;
    }
  }

  #social,
  #social-link {
    display: flex;
  }

  #social {
    h3 {
      margin-right: 20px;
      color: $base-color;
    }

    #social-link a {
      color: #000;
      background-color: #aaa;
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