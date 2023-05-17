<template><router-view></router-view></template>

<script>
export default {
  name: "App",
};
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}
body {
  padding: 0;
  margin: 0;
}
.signup-parent-div,
.login-parent-div {
  display: flex;
  gap: 100px;
  align-items: center;
  justify-content: center;
  margin-top: 100px;
}

.signup-logo {
  width: 600px;
  height: 400px;
  margin-top: 20px;
}
.register input,
.login input,
.add input {
  width: 400px;
  height: 40px;
  padding-left: 20px;
  display: block;
  margin-bottom: 30px;
  margin-right: auto;
  margin-left: auto;
  border: 1px solid skyblue;
}
.register button,
.login button,
.add button {
  width: 320px;
  height: 40px;
  border: 1px solid skyblue;
  background: skyblue;
  color: white;
  cursor: pointer;
}
</style>
