<template>
  <div>
    <div>{{ message }}</div>
  </div>
</template>

<script lang="ts">
import { mixins } from "vue-class-component";
import { Component, Prop, Vue } from "vue-property-decorator";
// import { VNodeDirective } from "vue/types/umd";
const GreetingProps = Vue.extend({
  props: {
    name: String,
  },
});

// Use `mixins` helper to combine defined props and a mixin.
@Component
export default class Greeting extends mixins(GreetingProps) {
  get message(): string {
    this.name = this.hello();
    return "Hello, " + this.name;
  }

  hello(): string {
    let nameinstring = prompt("Enter Name : ");
    if (!nameinstring) {
      return "";
    } else return nameinstring.toString();
  }
}
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
