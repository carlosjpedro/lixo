<template>
  <div>
    <h2><strong>UserName :</strong> {{ username }}</h2>
    <h3><strong>Age :</strong> {{ age }}</h3>
  </div>
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
  }
};
</script>