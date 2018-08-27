<template>
  <div class="tasks">
    <h3>{{name}}</h3>
    <ul>
      <slot></slot>
    </ul>
  </div>
</template>

<script>
export default {
  name: 'tasks',
  props: {
    name: {default: "List"},
  }
  }
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h3 {
  margin: 40px 0 0;
}
ul {
  list-style-type: none;
  padding: 0;
  max-width: 400px;
  margin: 0 auto;
}
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
