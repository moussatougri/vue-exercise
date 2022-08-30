<template>
  <button @click="addUser($event)">Add user</button>
</template>

<script>
export default {
  methods: {
    addUser(event) {
      event.preventDefault;
      this.$emit("new-user", { name: "Chris", age: 17, showAge: false });
    },
  },
};
</script>
