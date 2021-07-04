<template>
  <h1>{{ title }}</h1>
  <input type="text" ref="name" />
  <button @click="hadleClick">Click Me</button>
</template>

<script>

export default {
  name: 'App',
  data(){ 
    return {
      title: "My First Vue App"
    }
  },
  methods : {
    hadleClick() {
      console.log(this.$refs.name)
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
h1 {
  border-bottom: 1px solid #ddd;
  display: inline-block;
  padding-bottom: 10px;
}
</style>
