<template>
  <div class="wrapper">
    <Screen
      :currentNum="this.currentNum"
      :operation="this.operation"
      :prevNum="this.prevNum"
    />
    <Keypad
      @setCurrentNum="setCurrentNum"
      @setOperation="setOperation"
      @calculate="calculate"
      @clear="clear"
      @deleteNum="deleteNum"
    />
  </div>
</template>

<script>
import Keypad from "./Keypad.vue";
import Screen from "./Screen.vue";

export default {
  components: { Screen, Keypad },
  data() {
    return {
      currentNum: "",
      operation: "",
      prevNum: "",
    };
  },
  methods: {
    setCurrentNum(num) {
      this.currentNum += num;
    },
    setOperation(operation) {
      this.operation = operation;
      this.prevNum = this.currentNum;
      this.currentNum = "";
    },
    calculate() {
      if (this.operation === "*") this.multiply();
      else if (this.operation === "/") this.divide();
      else if (this.operation === "%") this.percentage();
      else if (this.operation === "-") this.subtract();
      else if (this.operation === "+") this.sum();
      this.prevNum = "";
      this.operation = "";
    },
    multiply() {
      this.currentNum = this.prevNum * this.currentNum;
    },
    divide() {
      this.currentNum = this.prevNum / this.currentNum;
    },
    percentage() {
      this.currentNum = this.currentNum / 100;
    },
    subtract() {
      this.currentNum = this.prevNum - this.currentNum;
    },
    sum() {
      this.currentNum = +this.prevNum + +this.currentNum;
    },
    clear() {
      this.currentNum = "";
      this.prevNum = "";
      this.operation = "";
    },
    deleteNum() {
      this.currentNum = this.currentNum.slice(0, -1);
    },
  },
};
</script>

<style scoped>
.wrapper {
  padding: 25px;
  border-radius: 10px;
  background-color: white;
  box-shadow: 0px 5px 10px 0px lightgray;
}
</style>
