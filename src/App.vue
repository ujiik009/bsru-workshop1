<template>
  <div id="app">
    <Header />
    <Content
      v-for="(car_item, index) in cars"
      :color="car_item.color"
      :name="car_item.name"
      :key="index"
    >
    <h1>
      slot body
    </h1>
    </Content>

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
          color: "#FFFFFF",
        }
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
