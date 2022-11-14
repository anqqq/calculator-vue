<template>
  <div class="keypad">
    <button @click="pressed('c')">C</button>
    <button @click="pressed('()')">()</button>
    <button @click="pressed('%')">%</button>
    <button @click="pressed('/')">/</button>

    <button @click="pressed('7')">7</button>
    <button @click="pressed('8')">8</button>
    <button @click="pressed('9')">9</button>
    <button @click="pressed('*')">x</button>

    <button @click="pressed('4')">4</button>
    <button @click="pressed('5')">5</button>
    <button @click="pressed('6')">6</button>
    <button @click="pressed('-')">-</button>

    <button @click="pressed('1')">1</button>
    <button @click="pressed('2')">2</button>
    <button @click="pressed('3')">3</button>
    <button @click="pressed('+')">+</button>

    <button @click="negateValue">+/-</button>
    <button @click="pressed('0')">0</button>
    <button @click="pressed('.')">.</button>
    <button @click="pressed('=')">=</button>
  </div>
</template>

<script>
export default {};
</script>

<style>
.keypad {
  border-radius: 2rem;
  font-size: 1.4rem;
  height: 23rem;

  display: grid;
  grid-template-columns: repeat(4, minmax(4rem, 1fr));
  grid-gap: 0.5rem;
}

.keypad button {
  display: flex;
  justify-content: center;
  align-items: center;
  color: white;
  background-color: #171717;
  border-radius: 45%;
  font-size: 16pt;
}

.keypad button:nth-child(1) {
  color: red;
}
.keypad button:nth-child(2),
button:nth-child(3),
button:nth-child(4),
button:nth-child(8),
button:nth-child(12),
button:nth-child(16) {
  color: green;
}

.keypad button:nth-child(20) {
  background-color: #30c117;
  color: black;
}
button:focus {
  outline: none;
}
</style>
