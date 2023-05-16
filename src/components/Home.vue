<template>
  <h1>Home Page</h1>
</template>
<script>
export default {
  name: "MyHome",
  mounted() {
    let user = localStorage.getItem("User-Info");
    if (!user) {
      this.$router.push({ name: "SignUp" });
    }
  },
};
</script>
