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
          description: "Boris die Kuh lebt auf einem malerischen Bauernhof im Herzen des ländlichen Idylls. Mit ihrem schwarz-weißen Fell und den sanften Augen ist sie das Maskottchen der Bauernfamilie.",
          rating: 1,
          weight: "431kg",
          gender: "w"
        },
        {
          id: "2",
          imageUrl: "https://loremflickr.com/300/300/Pferd?random=2",
          productName: "Pferd",
          birthDate: "20 Oktober, 2007",
          description: "Dieter das Pferd ist der stolze Hüter der weitläufigen Pferdekoppel. Sein glänzendes braunes Fell und seine kräftige Statur beeindrucken alle, die ihn sehen.  Dieter liebt es, über die grünen Hügel zu galoppieren. ",
          rating: 1,
          weight: "678kg",
          gender: "m"
        },
        {
          id: "3",
          imageUrl: "https://loremflickr.com/300/300/Esel?random=3",
          productName: "Esel",
          birthDate: "7 Mai, 2020",
          description: "Dave, der Esel, ist alles andere als gewöhnlich. Man nennt ihn liebevoll Dave der magische Käse Esel, denn in seinem Stall geschehen wunderbare Dinge. Jeden Morgen findet man dort frischen, köstlichen Käse",
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