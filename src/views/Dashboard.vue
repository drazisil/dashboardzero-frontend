<template>
  <div class="dashboardt">
    <h1>This is the dashboard page</h1>
    <h2>{{ message }}</h2>
  </div>
</template>

<script>
const axios = require("axios").default;

export default {
  name: "dashboard",
  data() {
    return {
      message: ""
    };
  },
  async mounted() {
    const response = await axios.get("http://localhost:4000");
    this.message = response.data.message;
  }
};
</script>
