<template>
  <div>
    <fabric-canvas :height="800" :width="800">
      <div v-for="(item, index) in robotMove" :key="`circle-${index}`">
        <fabric-circle
          :id="index"
          :left="item.left"
          :top="item.top"
          :radius="radius"
          :fill="fill"
          :selectable="false"
          :objectCaching="objectCaching"
        />
      </div>
      <div v-for="(item, index) in robotLine" :key="`line-${index}`">
        <fabric-line
          :id="index"
          :x1="item.headPosLeft"
          :y1="item.headPosTop"
          :x2="item.bodyPosLeft"
          :y2="item.bodyPosTop"
          :stroke="'gray'"
          :strokeWidth="3"
          :selectable="false"
          :evented="false"
        ></fabric-line>
      </div>
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
    FabricLine: vueFabricWrapper.FabricLine,
  },
  data() {
    return {
      radius: 3,
      fill: "#ffcc66",
      objectCaching: false,
      robotMove: [
        {left: 30, top: 40},
        {left: 50, top: 60},
        {left: 70, top: 80},
        {left: 85, top: 82},
        {left: 96, top: 104},
      ],
      robotLine: [
        {
          headPosLeft: 34,
          headPosTop: 44,
          bodyPosLeft: 50,
          bodyPosTop: 60,
        },
        {
          headPosLeft: 54,
          headPosTop: 64,
          bodyPosLeft: 70,
          bodyPosTop: 80,
        },
        {
          headPosLeft: 74,
          headPosTop: 84,
          bodyPosLeft: 85,
          bodyPosTop: 82,
        },
        {
          headPosLeft: 89,
          headPosTop: 86,
          bodyPosLeft: 96,
          bodyPosTop: 104,
        },
      ]
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