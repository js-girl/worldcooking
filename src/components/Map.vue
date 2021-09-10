<template>
  <div>
    <div id="overlay" v-show="showContent" v-on:click="closeModal">
      <div id="content">
        <div v-if="num === 0"><Egypt /></div>
        <div v-else-if="num === 1"><Morocco /></div>
        <div v-else-if="num === 2"><RSA /></div>
        <div v-else-if="num === 3"><Kankoku /></div>
        <div v-else-if="num === 4"><Taiwan /></div>
        <div v-else-if="num === 5"><Tyugoku /></div>
        <div v-else-if="num === 6"><Wasyoku /></div>
        <div v-else-if="num === 7"><Belarus /></div>
        <div v-else-if="num === 8"><England /></div>
        <div v-else-if="num === 9"><Finland /></div>
        <div v-else-if="num === 10"><France /></div>
        <div v-else-if="num === 11"><Germany /></div>
        <div v-else-if="num === 12"><Greece /></div>
        <div v-else-if="num === 13"><Hungary /></div>
        <div v-else-if="num === 14"><Italy /></div>
        <div v-else-if="num === 15"><Russia /></div>
        <div v-else-if="num === 16"><Sweden /></div>
        <div v-else-if="num === 17"><Swizerland /></div>
        <div v-else-if="num === 18"><Ukraine /></div>
        <div v-else-if="num === 19"><Saujiarabia /></div>
        <div v-else-if="num === 20"><Toruko /></div>
        <div v-else-if="num === 21"><America /></div>
        <div v-else-if="num === 22"><Canada /></div>
        <div v-else-if="num === 23"><Mexico /></div>
        <div v-else-if="num === 24"><Australia /></div>
        <div v-else-if="num === 25"><Newzealand /></div>
        <div v-else-if="num === 26"><Argentina /></div>
        <div v-else-if="num === 27"><Brazil /></div>
        <div v-else-if="num === 28"><Chile /></div>
        <div v-else-if="num === 29"><Peru /></div>
        <div v-else-if="num === 30"><Betonamu /></div>
        <div v-else-if="num === 31"><Firipin /></div>
        <div v-else-if="num === 32"><Indonesia /></div>
        <div v-else-if="num === 33"><Kitaindo /></div>
        <div v-else-if="num === 34"><Tai /></div>
      </div>
    </div>
    <div class="Gmap">
      <!-- <h1>Google Map</h1> -->
      <div class="map" ref="map" style="height: 500px; width: 90%"></div>
    </div>
  </div>
</template>

<script>
// Africa
import Egypt from "./Africa/Egypt.vue"
import Morocco from "./Africa/Morocco.vue"
import RSA from "./Africa/RSA.vue"
// EastAsia
import Kankoku from "./EastAsia/Kankoku.vue"
import Taiwan from "./EastAsia/Taiwan.vue"
import Tyugoku from "./EastAsia/Tyugoku.vue"
import Wasyoku from "./EastAsia/Wasyoku.vue"
// Europe
import Belarus from "./Europe/Belarus.vue"
import England from "./Europe/England.vue"
import Finland from "./Europe/Finland.vue"
import France from "./Europe/France.vue"
import Germany from "./Europe/Germany.vue"
import Greece from "./Europe/Greece.vue"
import Hungary from "./Europe/Hungary.vue"
import Italy from "./Europe/Italy.vue"
import Russia from "./Europe/Russia.vue"
import Sweden from "./Europe/Sweden.vue"
import Swizerland from "./Europe/Swizerland.vue"
import Ukraine from "./Europe/Ukraine.vue"
// Middleeast
import Saujiarabia from "./Middleeast/Saujiarabia.vue"
import Toruko from "./Middleeast/Toruko.vue"

// NouthAmerica
import America from "./NouthAmerica/America.vue"
import Canada from "./NouthAmerica/Canada.vue"
import Mexico from "./NouthAmerica/Mexico.vue"
// Oseania
import Australia from "./Oseania/Austlaria.vue"
import Newzealand from "./Oseania/Newzealand.vue"
// SouthAmerica
import Argentina from "./SouthAmerica/Argentina.vue"
import Brazil from "./SouthAmerica/Brazil.vue"
import Chile from "./SouthAmerica/Chile.vue"
import Peru from "./SouthAmerica/Peru.vue"
// SoutheastAsia
import Betonamu from "./SoutheastAsia/Betonamu.vue"
import Firipin from "./SoutheastAsia/Firipin.vue"
import Indonesia from "./SoutheastAsia/Indonesia.vue"
import Kitaindo from "./SoutheastAsia/Kitaindo.vue"
import Tai from "./SoutheastAsia/Tai.vue"
export default {
  components: {
    Egypt,
    Morocco,
    RSA,
    //
    Kankoku,
    Taiwan,
    Tyugoku,
    Wasyoku,
    //
    Belarus,
    England,
    Finland,
    France,
    Germany,
    Greece,
    Hungary,
    Italy,
    Russia,
    Sweden,
    Swizerland,
    Ukraine,

    Saujiarabia,
    Toruko,
    //
    America,
    Canada,
    Mexico,
    //
    Australia,
    Newzealand,
    //
    Argentina,
    Brazil,
    Chile,
    Peru,
    //
    Betonamu,
    Firipin,
    Indonesia,
    Kitaindo,
    Tai,
  },

  data() {
    return {
      showContent: false,

      map: "",
      myLatLng: { lat: 35.68, lng: 139.76 },
      num: 0,
      markers: [
        //〈ここにピンを立てる場所の緯度・経度を記入〉
        {
          name: "エジプト",
          lat: 30.1,
          lng: 31.4,
          food: "フムス",
          id: 0,
        },
        {
          name: "モロッコ",
          lat: 34.0208,
          lng: -6.84165,
          food: "クスクス",
          id: 1,
        },
        {
          name: "南アフリカ",
          lat: -33.59,
          lng: 25.36,
          food: "パップ",
          id: 2,
        },
        {
          name: "韓国",
          lat: 37.34,
          lng: 126.59,
          food: "キムチ",
          id: 3,
        },
        {
          name: "台湾",
          lat: 25.0329,
          lng: 121.5654,
          food: "魯肉飯",
          id: 4,
        },
        {
          name: "中国",
          lat: 35.0,
          lng: 105.0,
          food: "麻婆豆腐",
          id: 5,
        },
        {
          name: "日本",
          lat: 35.68,
          lng: 139.68,
          food: "和食御膳",
          id: 6,
        },
        {
          name: "ベラルーシ",
          lat: 53.54,
          lng: 27.34,
          food: "ドラニキ",
          id: 7,
        },
        {
          name: "イギリス",
          lat: 54.0,
          lng: -2.5,
          food: "アフタヌーンティー",
          id: 8,
        },
        {
          name: "フィンランド",
          lat: 60.17,
          lng: 24.93,
          food: "カレリアンピーラッカ",
          id: 9,
        },
        {
          name: "フランス",
          lat: 48.58,
          lng: 2.27,
          food: "エスカルゴ・ブルギニョオン",
          id: 10,
        },
        {
          name: "ドイツ",
          lat: 50.07,
          lng: 8.48,
          food: "ブラートヴルスト",
          id: 11,
        },
        {
          name: "ギリシャ",
          lat: 37.9666,
          lng: 23.7166,
          food: "ムサカ",
          id: 12,
        },
        {
          name: "パプリカシュチルケ",
          lat: 47.1624,
          lng: 19.5033,
          food: "和食御膳",
          id: 13,
        },
        {
          name: "イタリア",
          lat: 41.9027,
          lng: 12.4963,
          food: "ポレンタ",
          id: 14,
        },
        {
          name: "ロシア",
          lat: 60.0,
          lng: 100.0,
          food: "ピロシキ",
          id: 15,
        },
        {
          name: "スウェーデン",
          lat: 59.333,
          lng: 18.05,
          food: "ヤンソンの誘惑",
          id: 16,
        },
        {
          name: "スイス",
          lat: 46.8181,
          lng: 8.2275,
          food: "チーズフォンデュ",
          id: 17,
        },
        {
          name: "ウクライナ",
          lat: 50.45,
          lng: 30.5,
          food: "ボルシチ",
          id: 18,
        },
        {
          name: "サウジアラビア",
          lat: 24.6333,
          lng: 46.716667,
          food: "カプサ",
          id: 19,
        },
        {
          name: "トルコ",
          lat: 38.9637,
          lng: 35.2433,
          food: "ドネルケバブ",
          id: 20,
        },
        {
          name: "アメリカ",
          lat: 38.895111,
          lng: -77.036667,
          food: "ハンバーガー",
          id: 21,
        },
        {
          name: "カナダ",
          lat: 56.1303,
          lng: -106.3467,
          food: "プーティン",
          id: 22,
        },
        {
          name: "メキシコ",
          lat: 25.5405,
          lng: -103.326,
          food: "タコス",
          id: 23,
        },
        {
          name: "オーストラリア",
          lat: -33.52,
          lng: 151.12,
          food: "オーストラリアン・ミートパイ",
          id: 24,
        },
        {
          name: "ニュージーランド",
          lat: -40.9005,
          lng: 174.8859,
          food: "ハンギ料理",
          id: 25,
        },
        {
          name: "アルゼンチン",
          lat: -34.0,
          lng: -64.0,
          food: "アサード",
          id: 26,
        },
        {
          name: "ブラジル",
          lat: -18.8,
          lng: -47.9,
          food: "フェジョアーダ",
          id: 27,
        },
        {
          name: "チリ",
          lat: -33.45,
          lng: -70.55,
          food: "エンパナーダ",
          id: 28,
        },
        {
          name: "ペルー",
          lat: -11.9354,
          lng: -76.69,
          food: "アンティクーチョ",
          id: 29,
        },
        {
          name: "ベトナム",
          lat: 21.0333,
          lng: 105.83,
          food: "フォー",
          id: 30,
        },
        {
          name: "フィリピン",
          lat: 14.611,
          lng: 120.9962,
          food: "シニガン",
          id: 31,
        },
        {
          name: "インドネシア",
          lat: -6.2,
          lng: 106.8,
          food: "和食御膳",
          id: 32,
        },
        {
          name: "インド",
          lat: 20.5063,
          lng: 78.9628,
          food: "シナゴレン",
          id: 33,
        },
        {
          name: "タイ",
          lat: 13.7563,
          lng: 100.5017,
          food: "トムヤムクン",
          id: 34,
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
          const number = i

          const marker = new window.google.maps.Marker({
            position: {
              lat: this.markers[i].lat,
              lng: this.markers[i].lng,
            },
            // icon: {
            //   url: "../images/icon2.png",
            //   scaledSize: new window.google.maps.Size(10, 10),
            // },
            map: this.map,
          })

          const contentString =
            '<div class = "contentString">' +
            '<div class = "name">' +
            this.markers[i].name +
            "</div>" +
            '<div class = "food">' +
            this.markers[i].food +
            "</div>" +
            "</div>"

          const hoverinfo = new window.google.maps.InfoWindow({
            content: contentString,
          })
          marker.addListener("click", () => {
            this.num = number
            console.log(this.num)
          })
          marker.addListener("click", this.openModal)

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
      console.log(this.num)
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
  margin-top: 30px;
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
  padding: 10px;
  height: 90%;
  overflow-y: scroll;
}

#content::-webkit-scrollbar {
  display: none;
}

.contentString {
  flex-direction: column;
  display: flex;
  align-items: center;
  justify-content: center;
}
</style>
