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
  .card {
    height: 100%;

    text-align: left;

    img {
      aspect-ratio: 1;
      object-fit: cover;
      object-position: top;
    } 
  }

  h2 {
    font-size: 0.8rem;
    font-weight: 500;
  }
</style>