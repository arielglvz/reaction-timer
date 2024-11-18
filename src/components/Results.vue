<template>
   <p>Reaction Time: {{ score }} ms</p>
   <p class="rank">{{ rank }}</p>
</template>

<script>
export default {
  props: ['score'],
  data() {
    return {
      rank: null
    }
  },
  // Mounted Hook- this will fire as soon as the component mounted to the DOM
  mounted() {
    if (this.score < 250) {
      this.rank = 'Ninja Fingers'
    } else if(this.score < 400) {
      this.rank = 'Rapid Reflexes'
    } else {
      this.rank = 'Snail Pace...'
    }
  }
}
</script>

<style>
  .rank {
    font-style: 1.4em;
    color: #0faf87;
    font-weight: bold;
  }
</style>