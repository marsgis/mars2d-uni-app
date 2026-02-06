<template>
  <div id="mars2dContainer" class="mars2d-container"></div>
</template>

<!--<script module="mars2d" lang="renderjs">-->
<script>
import "leaflet/dist/leaflet.css";
import L from "leaflet";

import "mars2d/mars2d.css";
import * as mars2d from "mars2d";
import "mars2d-esri";

import { mapOptions } from "./config.js";

export default {
  data() {
    return {
      title: "mars2d",
    };
  },
  mounted() {
    this.createMap();
  },
  methods: {
    //创建地图
    createMap() {
      var map = new mars2d.Map("mars2dContainer", mapOptions);
      console.log("map构造完成", map);
    },
  },
};
</script>

<style></style>
