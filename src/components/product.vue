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
            <small class="card-text" style="color: rgb(3, 169, 3);">Gewicht: {{ data.weight }}</small>
          </p>
          <p class="d-flex justify-content-center">
            <small class="card-text" style="color: rgb(3, 169, 3);">Geschlecht: {{ data.gender }}</small>
          </p>
          <p class="d-flex justify-content-center">
            <small class="card-text" style="color: rgb(3, 169, 3);">Geburt: {{ data.birthDate }}</small>
          </p>
      </div>
      <div class="col-md-8">
        <div class="card-body">
          <h5 class="card-title" style="color: green;">{{ data.productName }}</h5>
          <p class="card-text">{{ data.description }}</p>
          <Rating :initalRating="data.rating" />
          <p><button type="button" class="btn btn-dark">Bewerten</button></p>
        </div>
      </div>
    </div>
  </div>
</template>