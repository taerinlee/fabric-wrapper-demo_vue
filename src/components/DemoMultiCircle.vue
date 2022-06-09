<template>
  <div>
    <fabric-canvas :height="800" :width="800">
      <fabric-circle
        v-bind:key="index"
        v-for="index in 100"
        :id="3"
        :left="getRandomInt(500)"
        :top="getRandomInt(500)"
        :radius="radius"
        :fill="getRainbow(5)"
        :objectCaching="objectCaching"
      />
    </fabric-canvas>
  </div>
</template>

<script>
import vueFabricWrapper from "vue-fabric-wrapper";

export default {
  name: "DemoMultiCircle",
  components: {
    FabricCanvas: vueFabricWrapper.FabricCanvas,
    FabricCircle: vueFabricWrapper.FabricCircle,
  },
  data() {
    return {
      radius: 3,
      objectCaching: false,
    };
  },
  methods: {
    getRandomInt(max) {
      return Math.floor(Math.random() * max);
    },
    getRainbow(max) {
      const rainbow = ["#ffcc66", "#ccff66", "#66ccff", "#ff6fcf", "#ff6666"];
      return rainbow[Math.floor(Math.random() * max)];
    }
  }
};
</script>