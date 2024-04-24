<template>
  <HeaderComponent/>
  <SliderSellFlowers/>
  <SliderInformation/>
</template>
<script>

import { RouterLink, RouterView } from 'vue-router'
import HeaderComponent from './components/Header/HeaderComponent.vue';
import SliderSellFlowers from './components/SliderSellFlowers/SliderSellFlowers.vue';
import SliderInformation from './components/SliderInformation/SliderInformation.vue';

export default {
  name: 'App',
  components: {
    HeaderComponent,
    SliderSellFlowers,
    SliderInformation,

  },
};
</script>