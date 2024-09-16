<script>
export default {
  data() {
    return {
      
    }
  }
}
</script>

<template>
  <main>
    <div class="container-lg">
      <p>--> Main content goes here<--</p>
    </div>
  </main>
</template>

<style lang="scss" scoped>
  @use '../styles/general.scss' as *;
  
  main {
    min-height: 200px;
    font-size: 1.2rem;
    color: #fff;
    background-color: #333;
  }

  p {
    height: 100%;
    padding: 100px 0;
    vertical-align: middle;
  }
</style>