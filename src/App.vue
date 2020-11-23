<template>
  <div id="app">
   <!-- <layout/> 
   <container/>
   <froms/>
   <silder/>-->
   <!-- <carrousel/> 
   <tabs/>-->
   <swipers/>
  </div>
</template>

<script>
import layout from "./components/layout.vue";
import container from "./components/container.vue"
import froms from "./components/froms.vue"
import silder from "./components/silder.vue"
import carrousel from "./components/s_tab.vue"
import Tabs from "./components/tabs/Tabs"
import Swiper from "./components/swiper/swipers"
import Swipers from './components/swiper/swipers.vue';
export default {
  name: "App",
  components: {
    layout,
    container,
    froms,silder,
    carrousel,
    Tabs,
    Swipers
  }
};
</script>

<style lang="less">

</style>
