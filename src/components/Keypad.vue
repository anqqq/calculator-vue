<template>
  <div class="keypad">
    <button @click="$emit('clear')">AC</button>
    <button @click="$emit('deleteNum')">C</button>
    <button @click="$emit('setOperation', '%')">%</button>
    <button @click="$emit('setOperation', '/')">/</button>

    <button @click="$emit('setCurrentNum', 7)">7</button>
    <button @click="$emit('setCurrentNum', 8)">8</button>
    <button @click="$emit('setCurrentNum', 9)">9</button>
    <button @click="$emit('setOperation', '*')">x</button>

    <button @click="$emit('setCurrentNum', 4)">4</button>
    <button @click="$emit('setCurrentNum', 5)">5</button>
    <button @click="$emit('setCurrentNum', 6)">6</button>
    <button @click="$emit('setOperation', '-')">-</button>

    <button @click="$emit('setCurrentNum', 1)">1</button>
    <button @click="$emit('setCurrentNum', 2)">2</button>
    <button @click="$emit('setCurrentNum', 3)">3</button>
    <button @click="$emit('setOperation', '+')">+</button>

    <button>+/-</button>
    <button @click="$emit('setCurrentNum', 0)">0</button>
    <button @click="$emit('setCurrentNum', '.')">.</button>
    <button @click="$emit('calculate')">=</button>
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
