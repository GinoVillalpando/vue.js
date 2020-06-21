<template>
  <div class="header">
    <h1>{{ msg }}</h1>
    <h2>{{ about }}</h2>
  </div>
</template>

<script>
export default {
  name: 'Header',
  props: {
    msg: String,
    about: String
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
  .header {
    background-color: #333;
    margin-bottom: 2rem;
    padding: 1.5rem;
    display: flex;
    justify-content: center;
  }
</style>
