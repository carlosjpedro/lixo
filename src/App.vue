<template>
  <h1>Contact Manager</h1>
  <active-user :username="user.username" :age="user.age" />
  <user-data
    :username="user.username"
    :age="user.age"
    @username-updated="updateUsername"
    @age-updated="updateAge"
  />
</template>

<script>
export default {
  data() {
    return {
      user: {
        username: "cpedro",
        age: 43,
      },
    };
  },
  methods: {
    updateUsername(username) {
      this.user.username = username;
    },
    updateAge(age) {
      this.user.age = age;
    },
  },
};
</script>

<style>
</style>