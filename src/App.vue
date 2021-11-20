<template>
  <div id="app">
    <Header />
    <Content
      v-for="(car_item, index) in cars"
      :color="car_item.color"
      :name="car_item.name"
      :key="index"
    />

    <Footer />
  </div>
</template>

<script>
import Header from "@/components/Header.vue";
import Content from "@/components/Content.vue";
import Footer from "@/components/Footer.vue";
export default {
  name: "App",
  components: {
    Header,
    Content,
    Footer,
  },
  data() {
    return {
      cars: [
        {
          name: "car 1",
          color: "green",
        },
        {
          name: "car 2",
          color: "red",
        },
      ],
    };
  },
};
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
