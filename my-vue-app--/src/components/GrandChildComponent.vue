<template>
    <div>
      <h4>GrandChild Component</h4>
      <button @click="emitData">Kirim Data ke Parent</button>
    </div>
  </template>
  
  <script>
  export default {
    name: 'GrandChildComponent',
    methods: {
      emitData() {
        this.$emit('data-emitted', 'Hello from GrandChildComponent!');
      }
    }
  };
  </script>
  
  <style scoped>
  h4 {
    color: #e74c3c;
  }
  button {
    margin-top: 10px;
    padding: 5px 10px;
    background-color: #e74c3c;
    color: white;
    border: none;
    border-radius: 4px;
  }
  </style>
  