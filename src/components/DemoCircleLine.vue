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
        {left: 108, top: 115}, 
        {left: 115, top: 128},
        {left: 127, top: 135},
        {left: 138, top: 145},
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
        {
          headPosLeft: 100,
          headPosTop: 108,
          bodyPosLeft: 108,
          bodyPosTop: 115,
        },
        {
          headPosLeft: 112,
          headPosTop: 119,
          bodyPosLeft: 115,
          bodyPosTop: 128,
        },
        {
          headPosLeft: 119,
          headPosTop: 132,
          bodyPosLeft: 127,
          bodyPosTop: 135,
        },
        {
          headPosLeft: 131,
          headPosTop: 139,
          bodyPosLeft: 138,
          bodyPosTop: 145,
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