<template>
<view class='startPage'>
  <image class="galochka" :source="require('../assets/galochka.png')" />
  <touchable-opacity class='FindInvestorTap' v-bind:on-press="() => toReg('indInvestor')">
    <text class='FindInvestor'> Найти инвестора</text>
  </touchable-opacity>
  <touchable-opacity class='FindStartupTap' v-bind:on-press="() => toReg('FindStartup')">
    <text class='FindStartup'> Найти стартап</text>
  </touchable-opacity>
  <image class="xmark" :source="require('../assets/xmark.png')" />
  <touchable-opacity class='selectScreen' v-bind:on-press="selectScreen">
    <text class='selectScreenText'> Войти</text>
  </touchable-opacity>

</view>
</template>


<script>
export default {
  props: {
    route: {
      Type: Object
    }
  },
  methods: {
    toReg(data) {
      this.$emit('toReg', data)
    },
    selectScreen() {
      this.$emit('selectScreen', 'login')
    }
  }
};
</script>

<style >
.startPage {
  flex: 1;
  align-items: center;
  justify-content: center;
  position: relative;
}

.FindInvestorTap {}

.FindInvestor {
  font-size: 38;
  background-color: #A0FFB0;
  border-radius: 15;
  padding-right: 10;
}

.FindStartup {
  font-size: 38;
}

.FindInvestorTap,
.FindStartupTap {
  justify-content: center;
  align-items: center;
}

.selectScreen {
  position: absolute;
  bottom: 20;
  right: 10;
}

.selectScreenText {
  font-size: 29px;
  line-height: 44px;
}

.galochka {
  position: absolute;
  top: 60;
  left: 10;
}

.xmark {
  position: absolute;
  bottom: 60;
  right: 10;
}
</style>
