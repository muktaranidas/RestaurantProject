<template>
  <img class="signup-logo" src="../assets/signup.jpg" alt="" />
  <h1>Login</h1>
  <div class="login">
    <input type="email" v-model="email" placeholder="Enter Email" />
    <input type="password" v-model="password" placeholder="Enter Password" />
    <button>Login</button>
    <p>
      New to Restaurant App? please
      <router-link to="/signup"> SignUp</router-link>
    </p>
  </div>
</template>
<script>
export default {
  name: "MyLogin",
};
</script>
