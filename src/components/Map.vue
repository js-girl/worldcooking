<template>
  <div class="Gmap">
    <h1>Google Map</h1>
    <div class="modal">
      <Modal @close="closeModal" v-if="modal" />
    </div>
    <div class="map" ref="map" style="height: 500px; width: 90%"></div>
  </div>
</template>

<script>
import Modal from "./Modal.vue"
export default {
  components: {
    Modal,
  },

  data() {
    return {
      modal: false,

      map: "",
      myLatLng: { lat: 35.68, lng: 139.76 },
      markers: [
        //〈ここにピンを立てる場所の緯度・経度を記入〉
        {
          name: "Tokyo",
          lat: 35.68,
          lng: 139.76,
          food: "和食御膳",
        },
        {
          name: "Australia",
          lat: -33.52,
          lng: 151.12,
          food: "ミートパイ",
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
    openModal() {
      this.modal = true
    },
    closeModal() {
      this.modal = false
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
</style>
