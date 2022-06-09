<template>
  <div>
    <fabric-canvas @canvas-updated="updateCanvas">
      <fabric-circle :id="3"></fabric-circle>
    </fabric-canvas>
    {{ json }}
  </div>
</template>

<script>
import vueFabricWrapper from "vue-fabric-wrapper";

export default {
  name: "DemoCircle",
  components: {
    FabricCanvas: vueFabricWrapper.FabricCanvas,
    FabricCircle: vueFabricWrapper.FabricCircle
  },
  data() {
    return {
      canvas: null
    };
  },
  methods: {
    updateCanvas(e) {
      this.canvas = e;
    }
  },
  computed: {
    json() {
      if (this.canvas) {
        return this.canvas.toJSON();
      }
      return "";
    }
  }
};
</script>
