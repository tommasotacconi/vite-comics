<script>
export default {
  data() {
    return {
      navItems: [
        'characters',
        'comics',
        'movies',
        'TV',
        'games',
        'collectibles',
        'videos',
        'fans',
        'news',
        'shop'
      ]
    }
  }
}
</script>

<template>
  <header>
    <div class="container-lg">
      <div class="logo-box">
        <img src="../assets/img/dc-logo.png" alt="">
      </div>
      <nav>
        <ul>
          <li v-for="navItem in navItems"><a href="">{{ navItem.toUpperCase() }}</a></li>
        </ul>
      </nav>
    </div>
  </header>
</template>

<style lang="scss" scoped>
  // Import general style
  @use '../styles/general.scss' as general-var;

  // custom properties for dimension
  $header-h: 120px;
  $li-border-w: 4.8px;


  header {
    height: $header-h;
  }

  .container-lg {
    display: flex;
    justify-content: space-between;

    .logo-box,
    ul {
      line-height: calc($header-h  - 2 * $li-border-w);      
    }

    img {
      height: 60%;
      vertical-align: middle;
    }

    ul {
      font-size: 0.7rem;
      font-weight: 600;
      height: 100%;
      display: flex;

      li {
        margin: 0 10px;
        border-block: $li-border-w solid transparent;
        
        &:hover {
          border-bottom-color: general-var.$base-color;
          
          a {
            color: general-var.$base-color;
          }
        }
      }
    }
  }
</style>