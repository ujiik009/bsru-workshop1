<template>
  <div>
    <h2>Content</h2>

    <!-- <div>{{ Number(num1) + Number(num2) }}</div>
    <div>
      First name : {{ info.first_name }} <br />
      Last Name : {{ info.last_name }}
      {{ info }}
    </div>
    <div>
      <input v-model="num1" />
      <input v-model="num2" />
    </div> -->
    <!-- <h1>v-text and v-html</h1> -->
    <!-- v-text -->
    <!-- <div v-text="username"></div>
    == {{ username }} -->

    <!-- v-html -->
    <!-- <div v-html="html_format"></div> -->

    <!-- <h1>v-show and v-if</h1>
    <div v-show="hiden == true">v-show Example</div>
    <div v-if="hiden == true">v-if Example</div> -->

    <!-- <h1>v-if and v-else</h1>
    <div v-if="number1 % 2 == 0">even</div>
    <div v-else>odd</div> -->

    <!-- <h1> v-for </h1>
    <div class="item" v-for="(car_item , index) in cars" :key="index">
      Car Name : {{car_item.name}} <br/>
      Car Color : {{car_item.color}}
    </div> -->

    <!-- <h1>v-on</h1>
    <div>
      Your Counter {{ counter }}
  
      <button @click="counter += 1">+</button>

      <button @click="counter -= 1">-</button>

      <select @change="counter += 1">
        <option value="green">green</option>
        <option value="blue">blue</option>
      </select>
    </div> -->

    <h1>Method</h1>
    <div>
      {{username}} : {{password}}
      <br/>
      <input type="text" v-model="username">
      <br/>
      <input type="password" v-model="password">
      <br/>
      <button @click="show_alert('Ice')"> Show Alert </button>
    </div>

    <Avatar />
  </div>
</template>
<script>
import Avatar from "@/components/Avatar.vue";
export default {
  components: {
    Avatar,
  },
  data() {
    return {
      counter: 0,
      number1: 2,
      hiden: true,
      username: "Apirat",
      password: "123456",
      num1: 0,
      num2: 0,
      info: {
        first_name: "Apirat",
        last_name: "Premachana",
      },
      html_format: "<h1>Hello</h1>",
      cars: [
        {
          name: "car 1",
          color: "green",
        },
        {
          name: "car 2",
          color: "blue",
        },
      ],
    };
  },
  methods:{
    show_alert(nickname){
      alert(this.username+":"+this.password+":"+nickname)
    }
  }
};
</script>

<style scoped>
.item {
  background-color: tomato;
  margin-bottom: 10px;
}
</style>