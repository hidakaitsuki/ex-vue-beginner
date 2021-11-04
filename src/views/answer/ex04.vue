<template>
  <div>
    <input type="text" v-model.number="num1" /><br />
    <input type="text" v-model.number="num2" /><br />
    <input type="text" v-model.number="num3" /><br />
    税抜き価格：{{ answer }}円 <br />
    税込み価格：{{ taxAnswer }}円
  </div>
</template>

<script lang="ts">
import Vue from "vue";
import Component from "vue-class-component";
@Component
export default class ex04 extends Vue {
  num1 = 0;
  num2 = 0;
  num3 = 0;
  readonly tax = 1.1;
  get answer() {
    return Number(this.num1 + this.num2 + this.num3).toLocaleString();
  }
  get taxAnswer() {
    return Number(
      this.num1 + this.num2 + this.num3 * this.tax
    ).toLocaleString();
  }
}
</script>

<style></style>
