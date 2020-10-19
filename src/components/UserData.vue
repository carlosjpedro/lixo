<template>
  <ul>
    <li>
      <label>username : </label>
      <input type="text" :value="username" @input="usernameChanged" />
    </li>
    <li>
      <label>age : </label>
      <input type="number" :value="age" @input="ageChanged" />
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
  setup(props, { emit }) {
    const ageChanged = function (event) {
      emit("age-updated", event.target.value);
    };
    const usernameChanged = function (event) {
      emit("username-updated", event.target.value);
    };

    return { ageChanged, usernameChanged };
  },
};
</script>