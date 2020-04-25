<template>
<view class="container">
  <!--
    Now we provide each todo-item with the todo object
    it's representing, so that its content can be dynamic.
    We also need to provide each component with a "key",
    which will be explained later.
  -->
  <start-page class="text-container" :route='route' />
</view>
</template>



<script>
import StartPage from "./src/StartPage";

export default {
  components: {
    StartPage
  },
  data: function() {
    return {
      route: 'StartPage'
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
