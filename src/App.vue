<template>
  <div id="app">
   <!-- <layout/> 
   <container/>
   <froms/>-->
   <silder/>
  </div>
</template>

<script>
import layout from "./components/layout.vue";
import container from "./components/container.vue"
import froms from "./components/froms.vue"
import silder from "./components/silder.vue"
export default {
  name: "App",
  components: {
    layout,
    container,
    froms,silder
  }
};
</script>

<style lang="less">

</style>
