<template>
  <div class="container">
    <Sidebar />
    <div class="map-content">
      <l-map
        v-if="showMap"
        :zoom="zoom"
        :center="center"
        :options="mapOptions"
        @update:center="centerUpdate"
        @update:zoom="zoomUpdate"
        class="map"
      >
        <l-tile-layer :url="url" :attribution="attribution" />
        <l-marker :lat-lng="withPopup">
          <l-icon :icon-url="icon" :icon-size="iconSize" />
          <l-popup>
            <div @click="innerClick"></div>
          </l-popup>
        </l-marker>
        <l-marker :lat-lng="withTooltip">
          <l-icon :icon-url="icon" :icon-size="iconSize" />
          <l-tooltip>
          </l-tooltip>
        </l-marker>
      </l-map>
      <Underbar
        :initial-drivers="driver"
        v-for="driver in drivers"
        :key="driver.id"
      />
    </div>
  </div>
</template>

<script>
import { latLng, Icon } from "leaflet";
import {
  LMap,
  LTileLayer,
  LMarker,
  LPopup,
  LTooltip,
  LIcon,
} from "vue2-leaflet";
import Sidebar from "../components/Sidebar";
import Underbar from "../components/Underbar";

const dummyData = {
  drivers: [
    {
      id: 1,
      car: "S336",
      start_time: "2022-01-31 08:30:32",
      end_time: "2022-01-31 19:30:30",
      records: [
        {
          frequency: 1,
          time: "2022-01-31 08:30:32",
          speed: "15",
          state: "行駛中",
          location: "新北市泰山區 貴鳳街",
          kilometer: "3553.1",
        },
        {
          frequency: 2,
          time: "2022-01-31 08:31:00",
          speed: "20",
          state: "行駛中",
          location: "新北市泰山區 貴鳳街",
          kilometer: "3553.1",
        },
      ],
    },
    {
      id: 2,
      car: "S337",
      start_time: "2022-02-01 08:30:32",
      end_time: "2022-02-01 19:30:30",
      records: [
        {
          frequency: 1,
          time: "2022-02-01 08:30:32",
          speed: "15",
          state: "行駛中",
          location: "新北市泰山區 貴鳳街",
          kilometer: "3553.1",
        },
        {
          frequency: 2,
          time: "2022-01-31 08:31:00",
          speed: "20",
          state: "行駛中",
          location: "新北市泰山區 貴鳳街",
          kilometer: "3553.1",
        },
      ],
    },
  ],
};

delete Icon.Default.prototype._getIconUrl;
Icon.Default.mergeOptions({
  iconRetinaUrl: require("leaflet/dist/images/marker-icon-2x.png"),
  iconUrl: require("leaflet/dist/images/marker-icon.png"),
  shadowUrl: require("leaflet/dist/images/marker-shadow.png"),
});

export default {
  name: "leaflet",
  components: {
    LMap,
    LTileLayer,
    LMarker,
    LPopup,
    LTooltip,
    LIcon,
    Sidebar,
    Underbar,
  },

  data() {
    return {
      drivers: [],
      zoom: 7,
      center: latLng(23.697809, 120.960518),
      url: "https://{s}.tile.openstreetmap.org/{z}/{x}/{y}.png",
      attribution:
        '&copy; <a href="http://osm.org/copyright">OpenStreetMap</a> contributors',
      withPopup: latLng(25.030694, 121.422887),
      withTooltip: latLng(25.031835, 121.421165),
      currentZoom: 20,
      currentCenter: latLng(25.030694, 121.422887),
      showParagraph: false,
      showMap: true,
      icon: require("../assets/22994_boat_icon.png"),
      iconSize: [30, 30],
    };
  },

  created() {
    this.fetchDrivers();
  },

  methods: {
    fetchDrivers() {
      this.drivers = dummyData.drivers;
    },

    zoomUpdate(zoom) {
      this.currentZoom = zoom;
    },

    centerUpdate(center) {
      this.currentCenter = center;
    },

    showLongText() {
      this.showParagraph = !this.showParagraph;
    },

    innerClick() {
      alert("Click!");
    },
  },
};
</script>

<style scoped>
.container {
  max-height: 100vh;
  width: 100%;
  display: flex;
}

.map-content {
  position: relative;
  width: 100%;
  max-height: 100vh;
}

.map {
  max-height: 100%;
}
</style>