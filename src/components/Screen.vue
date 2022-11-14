<template>
  <div class="screen">
    <!-- <small v-if="selectedOperation"
      >{{ prevNum }} {{ selectedOperation }} {{ currentNum }}</small
    > -->
    <small>11 - 5</small>
    <div>
      <h1>6</h1>
    </div>
  </div>
</template>

<script>
export default {};
</script>

<style>
.screen {
  text-align: right;
  margin-bottom: 20px;
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
