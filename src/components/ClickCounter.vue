<template>
  <div>
    <h1>{{ title }}</h1>
    <p>You've clicked the button {{ count }} times.</p>
    <button @click="incrementCounter">Click me</button>
  </div>
</template>

<script>
export default {
  data() {
    return {
      title: "Click Counter",
      count: 0
    };
  },
  methods: {
    incrementCounter() {
      this.count++;
    }
  }
};
</script>

<style scoped>
h1 {
  color: #42b983;
}
button {
  margin-top: 10px;
  padding: 10px;
  background-color: #42b983;
  color: white;
  border: none;
  cursor: pointer;
}
button:hover {
  background-color: #35495e;
}
</style>
