<template>
  <div>
    <p>名前：{{ name }}</p>
    <p>年齢：{{ age }}歳</p>
    <p>10年後の年齢：{{ add10year }}歳</p>
    <p>
      趣味：
      <span v-for="hobby of hobbies" v-bind:key="hobby">{{ hobby }}&nbsp;</span>
    </p>
    <a v-bind:href="url">ラクスパートナーズ</a><br />
    <img v-bind:src="imgurl" />
  </div>
</template>

<script lang="ts">
import Vue from "vue";
import Component from "vue-class-component";
@Component
export default class ex01 extends Vue {
  name = "日髙樹";
  age = 26;
  add10year = this.age + 10;
  hobbies = ["スイム", "バイク", "ラン"];
  url =
    "https://www.rakus-partners.co.jp/?gclid=EAIaIQobChMIj8eJxPj98wIVAWoqCh11AgfZEAAYASAAEgJoK_D_BwE";

  imgurl = "img/adpDSC_2005.jpg";
}
</script>

<style scoped>
div {
  width: 300px;
  border: solid;
  text-align: left;
}
img {
  width: 200px;
}
</style>
