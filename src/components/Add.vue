<template>
  <Navbar></Navbar>
  <h1>Add Page</h1>
</template>
<script>
import Navbar from "./Navbar.vue";
export default {
  name: "AddRestaurant",
  components: {
    Navbar,
  },

  mounted() {
    let user = localStorage.getItem("User-Info");
    if (!user) {
      this.$router.push({ name: "SignUp" });
    }
  },
};
</script>
