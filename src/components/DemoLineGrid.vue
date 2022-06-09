<template>
  <div>
    <fabric-canvas :id="'gridtesting'" :height="400" :width="400">
      <fabric-line-grid
        :id="'gridtesting1'"
        :gridSize="gridSize"
        :gridHeight="gridHeight"
        :gridWidth="gridWidth"
      ></fabric-line-grid>
      <fabric-rectangle :id="'rectGridTesting1'"></fabric-rectangle>
    </fabric-canvas>
    <table>
      <tr>
        <td>Grid Size:</td>
        <td>
          <input type="number" v-model.number="gridSize" min="10" />
        </td>
      </tr>
      <tr>
        <td>Grid Height:</td>
        <td>
          <input type="number" v-model.number="gridHeight" min="100" />
        </td>
      </tr>
      <tr>
        <td>Grid Width:</td>
        <td>
          <input type="number" v-model.number="gridWidth" min="100" />
        </td>
      </tr>
    </table>
  </div>
</template>

<script>
import vueFabricWrapper from "vue-fabric-wrapper";

export default {
  name: "DemoLineGrid",
  components: {
    FabricCanvas: vueFabricWrapper.FabricCanvas,
    FabricRectangle: vueFabricWrapper.FabricRectangle,
    FabricLineGrid: vueFabricWrapper.FabricLineGrid,
  },
  data() {
    return {
      gridSize: 20,
      gridHeight: 400,
      gridWidth: 400
    };
  },
  methods: {}
};
</script>
