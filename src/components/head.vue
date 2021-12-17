<template>
  <header>
    <div class="container">
      <div class="row">
          <div class="col-md-4 offset-md-1">
               <img :src="logo" class="app-logo" alt="logo">
          </div>
        <div class="col-md-6 my-auto">
          <h1>{{ title }}</h1>
        </div>
      </div>
    </div>
  </header>
</template>

<script>
export default {
  name: "Head",
  props: {
    title: {
      type: String,
      default: "Task Application",
    },
    logo: String,
  },
};
</script>

<style scoped>
.app-logo {
  border-radius: 80px;
  width: 80px;
  height: 80px;
}
</style>