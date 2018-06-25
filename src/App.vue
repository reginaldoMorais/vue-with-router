<template>
  <div id="app">
    <Header />
    <div class="container">
      <router-view/>
    </div>
  </div>
</template>

<script>
import Header from './components/Header';

export default {
  name: 'App',
  components: {
    Header,
  },
};
</script>

<style>
body {
  margin: 0;
}

#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  color: #2c3e50;
}

.container {
  max-width: 1140px;
  padding-right: 15px;
  padding-left: 15px;
  margin-right: auto;
  margin-left: auto;
}
</style>
