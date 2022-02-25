<template>
  <div>
    <v-carousel cycle>
      <v-carousel-item :src='this.$data.pizza1'>
      </v-carousel-item>
      <v-carousel-item :src='this.$data.pizza2'>
      </v-carousel-item>
      <v-carousel-item :src='this.$data.pizza3'>
      </v-carousel-item>
      <v-carousel-item :src='this.$data.pizza4'>
      </v-carousel-item>
    </v-carousel>
  </div>
</template>

<script>
import pizza1 from '../assets/pizza1.jpg'
import pizza2 from '../assets/pizza2.jpg'
import pizza3 from '../assets/pizza3.jpg'
import pizza4 from '../assets/pizza4.png'

  export default {
    name: 'HomeView',

    data() {
      return {
        pizza1,
        pizza2,
        pizza3,
        pizza4
      }
    },
  }
</script>
