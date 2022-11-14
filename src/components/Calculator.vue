<template>
  <div class="wrapper">
    <Screen />
    <Keypad />
  </div>
</template>

<script>
import Keypad from "./Keypad.vue";
import Screen from "./Screen.vue";

export default {
  name: "Calculator",
  components: { Screen, Keypad },
};
</script>

<style scoped>
.wrapper {
  padding: 10px;
  border-radius: 10px;
  background-color: white;
  box-shadow: 0px 5px 10px 0px lightgray;
}
</style>
