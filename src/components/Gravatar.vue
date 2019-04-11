<template>
  <div class="hello">
    <h1>{{ msg }}</h1>
    <input placeholder="Email" v-model="email">
    <br>
    <img :src="gravatarUrl">
  </div>
</template>

<script>
import md5 from "blueimp-md5";

export default {
  name: "Gravatar",
  props: {
    msg: String
  },
  data() {
    return {
      email: ""
    };
  },
  computed: {
    // a computed getter
    gravatarUrl: function() {
      // `this` points to the vm instance
      return `https://secure.gravatar.com/avatar/${md5(this.email)}?size=200`;
    }
  }
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h3 {
  margin: 40px 0 0;
}
ul {
  list-style-type: none;
  padding: 0;
}
li {
  display: inline-block;
  margin: 0 10px;
}
a {
  color: #42b983;
}
</style>
