<template>
  <div>
    <form>
      <input type="text" v-model.number="num1" />+
      <input type="text" v-model.number="num2" />=<span>{{ answer }}</span>
    </form>
  </div>
</template>

<script lang="ts">
import Vue from "vue";
import Component from "vue-class-component";

@Component
export default class ex03 extends Vue {
  private num1 = 0;
  private num2 = 0;
  private get answer() {
    return this.num1 + this.num2;
  }
}
</script>

<style></style>
