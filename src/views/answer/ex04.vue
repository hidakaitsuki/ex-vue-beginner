<template>
  <div>
    <input type="number" v-model.number="num1" /><br />
    <input type="number" v-model.number="num2" /><br />
    <input type="number" v-model.number="num3" /><br />
    税抜き価格：{{ answer.toLocaleString() }}円 <br />
    税込み価格：{{ taxAnswer.toLocaleString() }}円
  </div>
</template>

<script lang="ts">
import Vue from "vue";
import Component from "vue-class-component";
@Component
export default class ex04 extends Vue {
  private num1 = 0;
  private num2 = 0;
  private num3 = 0;
  readonly tax = 1.1;
  get answer() {
    return Number(this.num1) + Number(this.num2) + Number(this.num3);
  }
  get taxAnswer() {
    return Math.floor(
      (Number(this.num1) + Number(this.num2) + Number(this.num3)) * this.tax
    );
  }
}
</script>

<style></style>
