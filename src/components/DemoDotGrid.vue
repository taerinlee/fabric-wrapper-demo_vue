<template>
  <div>
    <fabric-canvas
      :id="'gridtesting2'"
      :height.sync="gridHeight"
      :width.sync="gridWidth"
    >
      <fabric-dot-grid
        :id="'gridtesting2'"
        :gridSize="gridSize"
        :gridHeight.sync="gridHeight"
        :gridWidth.sync="gridWidth"
      ></fabric-dot-grid>
      <fabric-rectangle :id="'rectGridTesting2'"></fabric-rectangle>
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
  name: "DemoDotGrid",
  components: {
    FabricCanvas: vueFabricWrapper.FabricCanvas,
    FabricRectangle: vueFabricWrapper.FabricRectangle,
    FabricDotGrid: vueFabricWrapper.FabricDotGrid
  },
  data() {
    return {
      gridSize: 40,
      gridHeight: 400,
      gridWidth: 400
    };
  },
  methods: {}
};
</script>
