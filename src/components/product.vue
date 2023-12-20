<script>
import Rating from "./rating.vue";

export default {
  props: {
    data: Object,
  },
  components: {
    Rating,
  },
};
</script>
<template>
  <div class="card mb-3" style="max-width: 540px">
    <div class="row no-gutters">
      <div class="col-md-4">
        <img :src="data.imageUrl" class="card-img" alt="..." />
          <p class="d-flex justify-content-center">
            <small class="card-text" style="color: rgb(9, 100, 9);">Gewicht: {{ data.weight }}</small>
          </p>
          <p class="d-flex justify-content-center">
            <small class="card-text" style="color: rgb(9, 100, 9);">Geschlecht: {{ data.gender }}</small>
          </p>
          <p class="d-flex justify-content-center">
            <small class="card-text" style="color: rgb(9, 100, 9);">Geburt: {{ data.birthDate }}</small>
          </p>
      </div>
      <div class="col-md-8">
        <div class="card-body">
          <h5 class="card-title" style="color: green;">{{ data.productName }}</h5>
          <p class="card-text">{{ data.description }}</p>
          <Rating :initalRating="data.rating" />
          <p class="d-flex justify-content-between">
            <button type="button" class="btn btn-outline-dark">Bewerten</button>
            <button type="button" class="btn btn-dark">Leihen</button>
          </p>
        </div>
      </div>
    </div>
  </div>
</template>git 