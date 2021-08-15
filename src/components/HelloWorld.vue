<template>
  <div>
    <div>
      <button @click="onclick">click me to input</button>
    </div>
  </div>
</template>

<script lang="ts">
import { Component, Prop, Vue } from "vue-property-decorator";

@Component
export default class HelloWorld extends Vue {
  letsgo = new go();
}
export class go {
  goname: string;
  consteuctor() {
    this.goname = "Abdullah Iqbal";
  }
  OnClicke(): void {
    console.log(this.goname);
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
