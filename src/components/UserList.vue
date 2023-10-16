<template>
    <div>
      <button v-for="user in users" :key="user" @click="highlightUsername(user)">
        {{ user }}
      </button>
    </div>
  </template>
  
  <script>
  export default {
    props: {
      users: Array,
    },
    methods: {
      highlightUsername(username) {
        this.$emit("user_clicked", username);
      },
    },
  };
  </script>
  