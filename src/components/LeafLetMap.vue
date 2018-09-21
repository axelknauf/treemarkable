<template>
  <l-map class="map" :zoom="zoom" :center="center">
    <l-tile-layer :url="url" :attribution="attribution"></l-tile-layer>
    <l-marker :lat-lng="marker"></l-marker>
  </l-map>
</template>

<script>
import { LMap, LTileLayer, LMarker } from "vue2-leaflet";
import L from "leaflet";

export default {
  name: "LeafLetMap",
  components: {
    LMap,
    LTileLayer,
    LMarker
  },
  data: () => {
    return {
      zoom: 13,
      center: L.latLng(50.928, 6.89122),
      url: "http://{s}.tile.osm.org/{z}/{x}/{y}.png",
      attribution:
        '&copy; <a href="http://osm.org/copyright">OpenStreetMap</a> contributors',
      marker: L.latLng(50.928, 6.89122)
    };
  },
  props: {
    msg: String
  }
};
</script>

<style scoped lang="scss">
@import "~leaflet/dist/leaflet.css";

.map {
  max-width: 600px;
  max-height: 600px;

  border: 2px solid black;
}
</style>
