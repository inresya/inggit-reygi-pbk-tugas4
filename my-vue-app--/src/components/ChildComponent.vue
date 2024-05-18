<template>
    <div>
      <h3>Child Component</h3>
      <GrandChildComponent @data-emitted="handleDataEmitted"></GrandChildComponent>
    </div>
  </template>
  
  <script>
  import GrandChildComponent from './GrandChildComponent.vue';
  
  export default {
    name: 'ChildComponent',
    components: {
      GrandChildComponent
    },
    methods: {
      handleDataEmitted(data) {
        this.$emit('data-emitted', data);
      }
    }
  };
  </script>
  
  <style scoped>
  h3 {
    color: #3498db;
  }
  </style>
  