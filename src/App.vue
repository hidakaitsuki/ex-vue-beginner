<template>
  <div id="app">
    <div id="nav">
      <router-link to="/">Home</router-link> |
      <router-link to="/about">About</router-link>
    </div>
    <router-view />
    <h1>Exam answers</h1>
    <router-link to="/ex01">Ex01</router-link>|
    <router-link to="/ex02">Ex02</router-link>|
    <router-link to="/ex03">Ex03</router-link>|
    <router-link to="/ex04">Ex04</router-link>|
    <router-link to="/ex05">Ex05</router-link>|
  </div>
</template>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}

#nav {
  padding: 30px;
}

#nav a {
  font-weight: bold;
  color: #2c3e50;
}

#nav a.router-link-exact-active {
  color: #42b983;
}
</style>
