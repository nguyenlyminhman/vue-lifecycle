<template>
  <div class="hello">
    <h1>{{ msg }}</h1>
  </div>
</template>

<script>
export default {
  props: {
    msg: String
  },
  data() {
    return {
      beforeCreate: "data in beforeCreate",
      created: "data in created"
    };
  },
  beforeCreate() {
    console.log("beforeCreate()");
  },
  created() {
    console.log("created()");
  },
  beforeMount() {
    console.log("beforeMount()");
  },
  mounted() {
    console.log("mounted()");
  },
  beforeUpdate() {
    console.log("beforeUpdate()");
  },
  updated() {
    console.log("updated()");
  },
  beforeDestroy() {
    console.log("beforeDestroy()");
  },
  destroyed() {
    console.log("destroyed()");
  }
};
</script>
<style scoped>
</style>
