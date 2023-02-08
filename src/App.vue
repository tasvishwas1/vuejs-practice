<template>
  <div id="app">
    {{message}}
    <span v-if="seen">Now you see me</span>
    <ul>
      <li v-bind:key="todo" v-for="todo in todos">
        {{ todo.text }}
      </li>
    </ul>
  </div>
</template>

<script>

export default {
  name: 'App',
  data() {
    return {
      message: 'Hello Vue!',
      seen: true,
      todos: [
        { text: 'Learn JavaScript' },
        { text: 'Learn Vue' },
        { text: 'Build something awesome' }
      ]
    }
  }
}

</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
