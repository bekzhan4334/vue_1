<template>
  <div class="app-container">
    <user-Form @form-submit="handleSubmit" />
    <br>
    <br>
    <br>
    <user-Data :userData="userData" />
  </div>
</template>

<script>
export default {
  data() {
    return {
      userData: {}
    };
  },
  methods: {
    handleSubmit(data) {
      this.userData = data;
    }
  }
};
</script>

<style scoped>
.app-container {
  max-width: 600px;
  margin: 0 auto;
  padding: 20px;
  background-color: #f9f9f9;
  border: 1px solid #ddd;
  border-radius: 5px;
}
</style>
