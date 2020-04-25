<template>
<view class='login'>
  <text class='TitleText'>Вход</text>
  <text-input class='input' placeholder='login' v-model="logintext" />
  <text-input class='input' placeholder='password' v-model="regtext" />
  <touchable-opacity class='LogIn' v-bind:on-press="FindStartup">
    <text class='logintext'>Вход</text>
  </touchable-opacity>
</view>
</template>

<!-- TitleText -->

<script>
export default {
  props: {
    route: {
      Type: Object
    }
  },
  data: function() {
    return {
      logintext: '',
      regtext: ''
    };
  },
  methods: {
    FindInvestor() {
      console.log(2);
    },
    FindStartup() {
      console.log(1);
    }
  }
};
</script>

<style >
.input {
  background-color: #fff;
  height: 45;
  margin-top: 8;
  width: 300;
  padding-left: 5;
  border-color: #000;
  border-width: 1;
  border-radius: 15;
  font-size: 20;
}

.login {
  flex: 1;
  align-items: center;
  justify-content: center;
  position: relative;
}

.TitleText {
  width: 300;
  font-size: 38;
}

.logintext {
  font-size: 28;
  background-color: rgba(196, 196, 196, 0.5);
  margin-top: 5;
  border-radius: 15;
  padding-left: 20;
  padding-right: 20;
}


.LogIn {
  width: 300;
  justify-content: flex-end;
  align-items: flex-end;
}
</style>
