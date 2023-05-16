<template>
  <Navbar></Navbar>
  <h1>Update Page</h1>
</template>
<script>
import Navbar from "./Navbar.vue";
export default {
  name: "UpdateRestaurant",
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
