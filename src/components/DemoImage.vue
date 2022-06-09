<template>
  <div>
    <fabric-canvas :height="800" :width="800">
      <fabric-image
        :id="1"
        url="https://tunglocpet.com/wp-content/uploads/2017/10/cho-corgi-pembroke-tunglocpet-01.jpg"
      ></fabric-image>
    </fabric-canvas>
  </div>
</template>

<script>
import vueFabricWrapper from "vue-fabric-wrapper";

export default {
  name: "DemoImage",
  components: {
    FabricCanvas: vueFabricWrapper.FabricCanvas,
    FabricImage: vueFabricWrapper.FabricImageFromURL,
  },
};
</script>