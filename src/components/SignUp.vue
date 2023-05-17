<template>
  <div class="signup-parent-div">
    <img class="signup-logo" src="../assets/signup.jpg" alt="" />
    <div class="register">
      <h1 class="signup-heading">Sign Up</h1>
      <input type="text" v-model="name" placeholder="Enter Name" />
      <input type="email" v-model="email" placeholder="Enter Email" />
      <input type="password" v-model="password" placeholder="Enter Password" />
      <button v-on:click="signup">Sign Up</button>
      <p>
        Already have a account? Please
        <router-link to="/login" class="link-login"> Login</router-link>
      </p>
    </div>
  </div>
</template>
<script>
import axios from "axios";
export default {
  name: "SignUp",
  data() {
    return {
      name: "",
      email: "",
      password: "",
    };
  },
  methods: {
    async signup() {
      let result = await axios.post("http://localhost:3000/users", {
        email: this.email,
        password: this.password,
        name: this.name,
      });
      console.warn(result);
      if (result.status == 201) {
        localStorage.setItem("User-Info", JSON.stringify(result.data));
        this.$router.push({ name: "Home" });
      }
    },
  },

  mounted() {
    let user = localStorage.getItem("User-Info");
    if (user) {
      this.$router.push({ name: "Home" });
    }
  },
};
</script>
<style>
.signup-heading,
.link-login {
  color: blueviolet;
}
</style>
