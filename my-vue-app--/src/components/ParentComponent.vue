<template>
    <div>
      <h2>Parent Component</h2>
      <p>Data dari GrandChildComponent: {{ parentData }}</p>
      <ChildComponent @data-emitted="handleDataEmitted"></ChildComponent>
      <slot></slot>
    </div>
  </template>
  
  <script>
  import ChildComponent from './ChildComponent.vue';
  
  export default {
    name: 'ParentComponent',
    components: {
      ChildComponent
    },
    data() {
      return {
        parentData: ''
      };
    },
    methods: {
      handleDataEmitted(data) {
        this.parentData = data;
      }
    }
  };
  </script>
  
  <style scoped>
  h2 {
    color: #42b983;
  }
  </style>
  