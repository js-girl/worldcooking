<template>
  <div class="Gmap">
    <h1>Google Map</h1>
    <div class="map" ref="map" style="height: 500px; width: 90%"></div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      map: "",
      myLatLng: { lat: 35.68, lng: 139.76 },
      markers: [
        //〈ここにピンを立てる場所の緯度・経度を記入〉
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
      infoWindow: null,
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
              lng: this.markers[i]["lng"],
            },
            map: this.map,
          })
          this.infoWindow = new window.google.maps.InfoWindow({
            content: contentString,
          })

          // this.marker.addListener("click", function () {
          //   this.infowindow.open(this.map, this.marker)
          // })
        }
        const contentString = "<div>" + this.marker.name + "</div>"
      }
    }, 500)
  },
  // methods() {
  //   this.infoWindow = new window.google.maps.InfoWindow({
  //     content: "<div>" + this.marker.name + "</div>",
  //   })

  //   // marker.addListener("click", function () {
  //   //   infowindow.open(this.map, marker)
  //   // })
  // },
}

//<サンプル>
//  var infoWindow = new google.maps.InfoWindow({
//       content: '<div><h3 style="text-decoration:none;">3,280万円/㎡ 1.1億円/坪</h3> <span style="color:green;">千代田区丸の内2-4-1</span></div>'
//     });

//     marker.addListener('click', function() {
//       infoWindow.open(map, marker);
//     });
</script>

<style>
.Gmap {
  flex-direction: column;
  align-items: center;
  display: flex;
  color: #ffc9d2;
}
</style>
