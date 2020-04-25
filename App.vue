<template>
<view class="container">

  <start-page v-if='route == "startPage"' />
  <login v-if='route == "login"' />
  <reg v-if='route == "reg"' />
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
      route: 'login'
    };
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
