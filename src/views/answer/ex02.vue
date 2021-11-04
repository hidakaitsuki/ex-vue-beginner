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
    <img v-bind:src="imgurl" /><br />
    <button type="button" v-on:click="onclick">ボタン</button>
  </div>
</template>

<script lang="ts">
import Vue from "vue";
import Component from "vue-class-component";
@Component
export default class ex01 extends Vue {
  name = "";
  age = 0;
  add10year = 0;
  hobbies = new Array<string>();
  url = "";
  imgurl = "";
  onclick() {
    this.name = "日髙樹";
    this.age = 26;
    this.add10year = this.age + 10;
    this.hobbies = ["スイム", "バイク", "ラン"];
    this.url =
      "https://www.rakus-partners.co.jp/?gclid=EAIaIQobChMIj8eJxPj98wIVAWoqCh11AgfZEAAYASAAEgJoK_D_BwE";

    this.imgurl = "img/adpDSC_2005.jpg";
  }
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
