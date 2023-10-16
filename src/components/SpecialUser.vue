<template>
    <div>
      <h1 v-if="selectedUsername">Selected User: {{ selectedUsername }}</h1>
    </div>
  </template>
  
  <script>
  export default {
    props: {
      selectedUsername: String,
    },
  };
  </script>
  