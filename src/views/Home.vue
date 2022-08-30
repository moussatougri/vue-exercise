<!-- eslint-disable vue/multi-word-component-names -->
<template>
  <section id="home">
    <TheHeader />
    <TheFooter />
    <UserList :users="users" />
    <Message
      v-if="show"
      content="Awesome title"
      @hook:mounted="printMounted()"
    />
    <button @click="show = false">Click me</button>
  </section>
</template>

<script>
import TheHeader from "../components/TheHeader.vue";
import TheFooter from "../components/TheFooter.vue";
import UserList from "../components/UserList.vue";
import Message from "../components/MessageContent.vue";

export default {
  components: {
    TheHeader,
    TheFooter,
    UserList,
    Message,
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
    printMounted() {
      console.log("print Mounted");
    },
  },
};
</script>
