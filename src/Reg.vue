<template>
<view class='reg'>
  <text class='TitleText'>Регистрация в три этапа</text>
  <text-input class='input' placeholder='Почта' v-model="emailtext" />
  <text-input class='input' placeholder='Пароль' v-model="password" />
  <touchable-opacity class='reg' v-bind:on-press="FindStartup">
    <text class='regtext'>Верификация</text>
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
      emailtext: '',
      password: ''
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

.reg {
  flex: 1;
  align-items: center;
  justify-content: center;
  position: relative;
}

.TitleText {
  width: 300;
  font-size: 38;
}

.regtext {
  font-size: 28;
  background-color: rgba(196, 196, 196, 0.5);
  margin-top: 5;
  border-radius: 15;
  padding-left: 20;
  padding-right: 20;
}


.reg {
  width: 300;
  justify-content: flex-end;
  align-items: flex-end;
}
</style>
