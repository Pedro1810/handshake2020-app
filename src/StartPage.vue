<template>
<view class='startPage'>
  <touchable-opacity class='FindInvestorTap' v-bind:on-press="FindInvestor">
    <text class='FindInvestor'> Найти инвестора</text>
  </touchable-opacity>
  <touchable-opacity class='FindStartupTap' v-bind:on-press="FindStartup">
    <text class='FindStartup'> Найти стартап</text>
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
</style>
