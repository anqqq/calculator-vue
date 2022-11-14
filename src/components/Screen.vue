<template>
  <div class="screen">
    <small v-show="operation">
      {{ prevNum }} {{ operation }} {{ currentNum }}
    </small>
    <h1>{{ currentNum || 0 }}</h1>
  </div>
</template>

<script>
export default {
  props: {
    currentNum: String,
    prevNum: String,
    operation: String,
  },
};
</script>

<style>
.screen {
  text-align: right;
  margin-bottom: 20px;
  padding: 15px;
  border-radius: 10px;
  background-color: whitesmoke;
}
.screen small {
  font-weight: bold;
  color: rgb(185, 185, 185);
  font-size: 11pt;
}
.screen h1 {
  color: black;
  font-size: 2.5rem;
  font-weight: 600;
  letter-spacing: -1px;
}
</style>
