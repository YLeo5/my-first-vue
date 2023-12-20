<script>
import Product from "./product.vue";

export default {
  components: {
    Product,
  },
  data() {
    return {
      products: [
        {
          id: "1",
          imageUrl: "https://loremflickr.com/300/300/Kuh?random=1",
          productName: "Kuh",
          birthDate: "4 Juni, 2014",
          description: "Was ist besser als ein Esel, eine Kuh. Die Kuh ist super denn es kann alles machen ausser Kuchen backen.",
          rating: 1,
          weight: "431kg",
          gender: "w"
        },
        {
          id: "2",
          imageUrl: "https://loremflickr.com/300/300/Pferd?random=2",
          productName: "Pferd",
          birthDate: "20 Oktober, 2007",
          description: "Was ist besser als eine Kuh, ein Pferd. Das Pferd ist super denn sie kann alles machen ausser Kuchen backen.",
          rating: 1,
          weight: "678kg",
          gender: "m"
        },
        {
          id: "3",
          imageUrl: "https://loremflickr.com/300/300/Esel?random=3",
          productName: "Esel",
          birthDate: "7 Mai, 2020",
          description: "Was ist besser als ein Pferd, ein Esel. Der Esel ist super denn er kann alles machen ausser Kuchen backen.",
          rating: 1,
          weight: "349kg",
          gender: "unbestimmt"
        },
      ],
    };
  },
};
</script>
<template>
  <div v-for="product in products" :key="product.id">
    <Product :data="product" />
  </div>
</template>