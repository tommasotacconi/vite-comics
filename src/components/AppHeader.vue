<script>
export default {
  data() {
    return {
      
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
          <li><a href="">ELEMENTO LISTA</a></li>
          <li><a href="">ELEMENTO LISTA</a></li>
          <li><a href="">ELEMENTO LISTA</a></li>
          <li><a href="">ELEMENTO LISTA</a></li>
        </ul>
      </nav>
    </div>
  </header>
</template>

<style lang="scss" scoped>
  // Import general style
  @use '../styles/general.scss' as *;

  // custom properties for dimension
  $header-h: 120px;
  $li-border-w: 5px;


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
      list-style-type: none;

      li {
        margin: 0 10px;
        border-block: $li-border-w solid transparent;
        
        &:hover {
          border-bottom-color: $base-color;
          
          a {
            color: $base-color;
          }
        }
      }
    }
  }
</style>