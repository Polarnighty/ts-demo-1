<template>
  <div>
    <input type="text" v-model="text" />
    <button @click="addTodo">add</button>
  </div>
</template>
<script lang="ts">
import { Component, Vue } from "vue-property-decorator";
@Component
export default class NewTodo extends Vue {
  text = "";
  addTodo() {
    this.$emit("addTodo", this.text);
    this.text = "";
  }
}
</script>