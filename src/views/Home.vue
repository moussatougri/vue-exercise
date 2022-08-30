<!-- eslint-disable vue/multi-word-component-names -->
<template>
  <section id="home">
    <TheHeader />
    <TheFooter />
    <UserList :users="users" />
    <button @click="show = false">Click me</button>
    <AddUserButton @new-user="addUser" />
  </section>
</template>

<script>
import TheHeader from "../components/TheHeader.vue";
import TheFooter from "../components/TheFooter.vue";
import UserList from "../components/UserList.vue";
import AddUserButton from "../components/AddUserButton.vue";

export default {
  components: {
    TheHeader,
    TheFooter,
    UserList,
    AddUserButton,
  },
  data() {
    return {
      show: true,
      users: [
        { name: "Florian", age: 21, showAge: false },
        { name: "Peter", age: 54, showAge: false },
      ],
    };
  },

  methods: {
    addUser(newUser) {
      this.users.push(newUser);
    },
  },
};
</script>
