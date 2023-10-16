<template>
  <div id="app">
    <UserList :users="users" @user_clicked="highlight_username" />
    <SpecialUser :selectedUsername="selectedUsername" />
  </div>
</template>

<script>
import UserList from "./components/UserList.vue";
import SpecialUser from "./components/SpecialUser.vue";

export default {
  data() {
    return {
      users: ["User1", "User2", "User3"],
      selectedUsername: "",
    };
  },
  methods: {
    highlight_username(username) {
      this.selectedUsername = username;
    },
  },
  components: {
    UserList,
    SpecialUser,
  },
};
</script>
