<template>
  <div id="app">
    <div class="hello-wrold">
      <img alt="Vue logo" src="./assets/logo.png" />
      <div class="hello-wrold__message">
        {{ message }}
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "App",
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
