<script>
  export default {
    props: ['initialRating'],
    data() {
      return {
        rating: this.initialRating,
        color: 'green',
      }
    },
    methods: {
      assignRating(newRating) {
        this.rating = newRating
      }
    }
  }
</script>
<template>
  <span :style="{color: color}" v-on:click="assignRating(1)">
    <i v-if="rating >= 1" class="bi bi-star-fill"></i>
    <i v-else class="bi bi-star"></i>
  </span>
  <span :style="{color: color}" v-on:click="assignRating(2)">
    <i v-if="rating >= 2" class="bi bi-star-fill"></i>
    <i v-else class="bi bi-star"></i>
  </span>
  <span :style="{color: color}" v-on:click="assignRating(3)">
    <i v-if="rating >= 3" class="bi bi-star-fill"></i>
    <i v-else class="bi bi-star"></i>
  </span>
  <span :style="{color: color}" v-on:click="assignRating(4)">
    <i v-if="rating >= 4" class="bi bi-star-fill"></i>
    <i v-else class="bi bi-star"></i>
  </span>
  <span :style="{color: color}" v-on:click="assignRating(5)">
    <i v-if="rating >= 5" class="bi bi-star-fill"></i>
    <i v-else class="bi bi-star"></i>
  </span>
  <span :style="{color: color}" v-on:click="assignRating(6)">
    <i v-if="rating >= 6" class="bi bi-star-fill"></i>
    <i v-else class="bi bi-star"></i>
  </span>
  <small>({{rating}})</small>
</template>