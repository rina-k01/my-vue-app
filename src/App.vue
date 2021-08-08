<template>
  <div id="app">
    <div class="hello-wrold">
      <img alt="Vue logo" src="./assets/logo.png" />
      <div class="hello-wrold__message">
        {{ message }}
      </div>
    </div>
    <TodoList />
  </div>
</template>

<script>
import TodoList from "@/components/TodoList.vue"
export default {
  name: "App",
  components: {
    TodoList,
  },
  data: function () {
    return {
      message: "WebExpert Course Vue Template",
    }
  },
  methods: {},
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
}
</style>

<style scoped>
.hello-wrold {
  margin-top: 60px;
  text-align: center;
}

.hello-wrold .hello-world__message {
  color: #2c3e50;
}
</style>
