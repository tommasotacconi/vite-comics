<script>
export default {
  data() {
    return {
      
    }
  },
  props: [
    'Thumb',
    'Series'
  ]
}
</script>

<template>
  <div class="card">
    <div class="card-img">
      <img :src="Thumb" alt="img of {{ Series }}">
    </div>
    <h2>
      {{ Series }}
    </h2>
  </div>  
</template>

<style scoped>
</style>