<template>
  <h1>{{ latitude }}-{{ longitude }}</h1>
</template>

<script>
export default {
  data() {
    return {
      latitude: 42,
      longitude: 1179,
    };
  },
};
</script>

<style lang="scss">
h1 {
  margin-top: 100px;
  margin-left: 1em;
}
</style>
