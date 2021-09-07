<template>
  <div>
    <div v-for="food in all" :key="food.id">
      {{ food.name }}
    </div>
    <div>
      <img src="" alt="お店の名前" id="food-image" />
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return { all: [] };
  },
  methods: {
    getrestaurant: function() {
      this.axios
        .get(
          "hotpepper/gourmet/v1/?key=703a952c5ae9eaa7&large_area=Z011&format=json"
        )
        .then((res) => res.data)
        .then((value) => {
          this.all = value.results.shop;
        });
    },
  },
  mounted() {
    this.getrestaurant();
  },
};
</script>

<style></style>
