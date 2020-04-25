<template>
<view class='login'>
  <text class='MainTitleText'>Handshake2020</text>
  <text class='TitleText'>Вход</text>
  <text-input class='input1' placeholder='Логин' v-model="logintext" />
  <text-input class='input2' placeholder='Пароль' v-model="regtext" />
  <touchable-opacity class='LogIn' v-bind:on-press="FindStartup">
    <text class='logintext'>Войти</text>
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
.MainTitleText {
  position: absolute;
  top: 38;
  width: 300;
  font-size: 38;
}

.input1 {
  background-color: #fff;
  height: 45;
  margin-top: 16;
  width: 300;
  padding-left: 13;
  border-color: #000;
  border-width: 2;
  border-radius: 15;
  font-size: 20;
}

.input2 {
  background-color: #fff;
  height: 45;
  margin-top: 26;
  width: 300;
  padding-left: 13;
  border-color: #000;
  border-width: 2;
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
  margin-top: 18;
  border-radius: 15;
  padding-left: 27;
  padding-right: 27;
  padding-top: 5;
  padding-bottom: 5;
}


.LogIn {
  width: 300;
  justify-content: flex-end;
  align-items: flex-end;
}
</style>
