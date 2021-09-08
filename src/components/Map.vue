<template>
  <div>
    <button v-on:click="openModal">Click</button>
    <div id="overlay" v-show="showContent" v-on:click="closeModal">
      <div id="content">
        <Australia />
      </div>
    </div>
    <div class="Gmap">
      <!-- <h1>Google Map</h1> -->
      <div class="map" ref="map" style="height: 500px; width: 90%"></div>
    </div>
  </div>
</template>

<script>
import Wasyoku from "./EastAsia/Wasyoku.vue"
import Australia from "./Oseania/Austlaria.vue"
export default {
  components: {
    // Wasyoku,
    Australia,
  },

  data() {
    return {
      showContent: false,

      map: "",
      myLatLng: { lat: 35.68, lng: 139.76 },
      markers: [
        //〈ここにピンを立てる場所の緯度・経度を記入〉
        {
          name: "Tokyo",
          lat: 35.68,
          lng: 139.76,
          food: "和食御膳",
          component: Wasyoku,
        },
        {
          name: "Australia",
          lat: -33.52,
          lng: 151.12,
          food: "ミートパイ",
          component: Australia,
        },
      ],
    }
  },

  mounted() {
    console.log(window.google)
    let timer = setInterval(() => {
      if (window.google) {
        clearInterval(timer)
        this.map = new window.google.maps.Map(this.$refs.map, {
          center: this.myLatLng,
          zoom: 2,
        })
        for (let i = 0; i < this.markers.length; i++) {
          const marker = new window.google.maps.Marker({
            position: {
              lat: this.markers[i].lat,
              lng: this.markers[i].lng,
            },
            // icon: {
            //   url: "../images/icon1.png",
            //   scaledSize: new window.google.maps.Size(20, 20),
            // },
            map: this.map,
          })

          const contentString =
            '<div class = "name">' +
            this.markers[i].name +
            "</div>" +
            '<a href v-on:click="openModal">' +
            this.markers[i].food +
            "</a>"
          // +'<div id = "overlay">' +
          // "</div>"

          const infoWindow = new window.google.maps.InfoWindow({
            content: contentString,
          })

          const hoverinfo = new window.google.maps.InfoWindow({
            content: contentString,
          })

          marker.addListener("click", function () {
            infoWindow.open(this.map, marker)
          })
          marker.addListener("mouseover", function () {
            hoverinfo.open(this.map, marker)
          })
          marker.addListener("mouseout", function () {
            hoverinfo.close(this.map, marker)
          })
        }
      }
    }, 500)
  },
  methods: {
    openModal: function () {
      this.showContent = true
    },
    closeModal: function () {
      this.showContent = false
    },
  },
}
</script>

<style>
.Gmap {
  flex-direction: column;
  align-items: center;
  display: flex;
  color: #ffc9d2;
}

#overlay {
  /*要素を重ねた時の順番*/
  z-index: 2;

  /*画面全体を覆う設定*/
  position: fixed;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  background-color: rgba(0, 0, 0, 0.5);

  /*画面の中央に要素を表示させる設定*/
  display: flex;
  align-items: center;
  justify-content: center;
}

#content {
  z-index: 1;
  padding: 1em;
}
</style>
