<template>
  <div>
    <h1>Box Color Changer</h1>
    <div class="box" :style="{ backgroundColor: currentColor }"></div>
    <button @click="changeColor">Change Color</button>
  </div>
</template>

<script>
export default {
  data() {
    return {
      colors: ["#FF5733", "#33FF57", "#3357FF", "#FF33A1", "#33FFF0", "#F033FF"],
      currentColor: "#FF5733"  // Warna awal
    };
  },
  methods: {
    changeColor() {
      const randomIndex = Math.floor(Math.random() * this.colors.length);
      this.currentColor = this.colors[randomIndex];
    }
  }
};
</script>

<style scoped>
.box {
  width: 200px;
  height: 200px;
  margin: 20px auto;
  transition: background-color 0.5s ease;
}
button {
  padding: 10px 20px;
  background-color: #42b983;
  color: white;
  border: none;
  cursor: pointer;
}
button:hover {
  background-color: #35495e;
}
</style>
