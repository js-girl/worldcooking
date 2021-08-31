<template>
  <div>
    <h1>Google Map</h1>
    <div ref="map" style="height: 500px; width: 100%"></div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      map: "",
      myLatLng: { lat: 35.68, lng: 139.76 },
      markers: [
        {
          name: "Tokyo",
          lat: 35.68,
          lng: 139.76,
        },
        {
          name: "Australia",
          lat: -33.52,
          lng: 151.12,
        },
      ],
      marker: null,
      infoWindow: [],
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
          this.marker = new window.google.maps.Marker({
            position: {
              lat: this.markers[i]["lat"],
              lng: this.marker[i]["lng"],
            },
            map: this.map,
          })
        }
      }
    }, 500)
  },
}
</script>

<style></style>
