<template>
<view class="container">

  <start-page @selectScreen='selectScreen' @toReg='toReg' v-if='route == "startPage"' />
  <login v-if='route == "login"' />

  <reg v-if='route == "reg"' :typeOfRegistration='typeOfRegistration' />

</view>
</template>

<script>
import StartPage from "./src/StartPage";
import login from "./src/Login";
import reg from "./src/Reg";

export default {
  components: {
    StartPage,
    login,
    reg
  },
  data: function() {
    return {
      route: 'startPage',
      typeOfRegistration: ''

    };
  },
  methods: {
    toReg(data) {
      this.typeOfRegistration = data;
      this.route = 'reg';

      console.log('Тип регестрации: ' + data);
    },
    selectScreen(data) {
      this.route = data;
    }
  }

};
</script>


<style>
.container {
  background-color: white;
  align-items: center;
  justify-content: center;
  flex: 1;
}

.text-container {
  color: blue;
  padding: 2;
  font-size: 22;
}

.text-input-container {
  width: 300;
  height: 40;
  font-size: 22;
  border-color: gray;
}
</style>
