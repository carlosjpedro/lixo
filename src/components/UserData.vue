<template>
  <ul>
    <li>
      <label>username : </label>
      <input type="text" v-model="username" @input="usernameChanged" />
    </li>
    <li>
      <label>age : </label>
      <input type="number" v-model="age" @input="ageChanged" />
    </li>
  </ul>
</template>

<script>
export default {
  props: {
    username: {
      required: true,
      type: String,
    },
    age: {
      required: true,
      type: Number,
    },
  },
  emits: ["username-updated", "age-updated"],
  methods: {
    ageChanged(event) {
      this.$emit("age-updated", event.target.value);
    },
    usernameChanged(event) {
      this.$emit("username-updated", event.target.value);
    },
  },
};
</script>