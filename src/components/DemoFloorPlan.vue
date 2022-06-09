<template>
  <div class="hello">
      <div class="scoped__canvas-wrapper">
        <fabric-canvas class="scoped__canvas js-canvas" :height="800" :width="800">
            <fabric-rectangle
                    :id="3"
                    :left="this.meetingRoomRect.left"
                    :top="this.meetingRoomRect.top"
                    originX="left"
                    originY="top"
                    :width="this.meetingRoomRect.width"
                    :height="this.meetingRoomRect.height"
                    :angle="this.meetingRoomRect.angle"
                    fill="rgba(255,0,0,0.5)"
                    :transparentCorners="false"
                />
        </fabric-canvas>
        <img
            class="scoped__image"
            src="https://online.visual-paradigm.com/repository/images/e5728e49-09ce-4c95-b83c-482deee24386.png"
            alt="floorplan provided by client"
        >
    </div>
  </div>
</template>

<script>
import vueFabricWrapper from "vue-fabric-wrapper";

export default {
  name: "DemoFloorPlan",
  components: {
    FabricCanvas: vueFabricWrapper.FabricCanvas,
    FabricRectangle: vueFabricWrapper.FabricRectangle,
  },
  data() {
    return {
      meetingRoomRect: {
        left: 50,
        top: 50,
        width: 50,
        height: 50,
        angle: -10
      }
    };
  }
};
</script>

<style>
.scoped__canvas-wrapper {
    position: relative;
  }
.scoped__canvas {
    position: absolute;
    top: 0;
    right: 0;
    bottom: 0;
    left: 0;
    z-index: 5;
    width: 100%;
    height: 100%;
  }
.scoped__image {
    position: relative;
    display: block;
    position: relative;
  }
</style>
