<template>
  <div id="app">
   <!-- <layout/> 
   <container/>
   <froms/>
   <silder/>-->
   <carrousel/>
  </div>
</template>

<script>
import layout from "./components/layout.vue";
import container from "./components/container.vue"
import froms from "./components/froms.vue"
import silder from "./components/silder.vue"
import carrousel from "./components/s_tab.vue"
export default {
  name: "App",
  components: {
    layout,
    container,
    froms,silder,
    carrousel
  }
};
</script>

<style lang="less">

</style>
