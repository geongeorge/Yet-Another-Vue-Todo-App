<template>
      <li><slot></slot></li>
</template>

<script>
export default {
  name: 'task',
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
li {
  display: block;
  margin: 20px 10px;
  padding: 15px;
  font-size: 20px;
  border: 1px dashed #aaa;
  border-radius: 5px;
}
a {
  color: #42b983;
}
</style>
