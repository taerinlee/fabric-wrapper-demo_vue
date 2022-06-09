<template>
  <div id="demo-triangle">
    <fabric-canvas>
      <fabric-circle :id="3"></fabric-circle>
      <fabric-triangle :id="1"></fabric-triangle>
    </fabric-canvas>
  </div>
</template>

<script>
import vueFabricWrapper from "vue-fabric-wrapper";

export default {
  name: "DemoTriangle",
  components: {
    FabricCanvas: vueFabricWrapper.FabricCanvas,
    FabricCircle: vueFabricWrapper.FabricCircle,
    FabricTriangle: vueFabricWrapper.FabricTriangle,
  }
};
</script>

<style>
#demo-triangle {
  font-family: "Avenir", Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
