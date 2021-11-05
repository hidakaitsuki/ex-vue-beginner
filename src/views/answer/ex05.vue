<template>
  <div>
    <p v-if="name === ''">名前が入力されていません</p>
    名前：<br /><input type="text" v-model="name" /> <br />
    <p v-if="age === ''">年齢が入力されていません</p>
    年齢：<br /><input type="text" v-model="age" /><br />
    <p v-if="comment === ''">コメントが入力されていません</p>
    コメント：<br /><textarea
      name=""
      id=""
      cols="30"
      rows="10"
      v-model="comment"
    ></textarea
    ><br />
    <hr />
    入力値：<br />
    名前：{{ name }}<br />
    年齢：{{ age }}<br />
    コメント：
    <pre>{{ comment }}</pre>
    <br />
  </div>
</template>

<script lang="ts">
import Vue from "vue";
import Component from "vue-class-component";
@Component
export default class ex05 extends Vue {
  private name = "";
  private age = "";
  private comment = "";
}
</script>

<style scoped>
div {
  text-align: left;
}
p {
  color: red;
}

</style>
