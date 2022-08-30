<!-- eslint-disable vue/multi-word-component-names -->
<template>
  <section id="home">
    <TheHeader />
    <TheFooter />
    <MapLi ref="myMap" />
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
import MapLi from "../components/MapLi.vue";

export default {
  components: {
    TheHeader,
    TheFooter,
    UserList,
    AddUserButton,
    MapLi,
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
  mounted() {
    console.log(`${this.$refs.myMap.latitude} - ${this.$refs.myMap.longitude}`);
  },

  methods: {
    addUser(newUser) {
      this.users.push(newUser);
    },
  },
};
</script>
