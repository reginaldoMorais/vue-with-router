<template>
  <div class="header">
    <a href="/"><img src="../assets/logo.png" class="logo"></a>
    <div class="nav">
      <a href="/" v-bind:class="isActive('HelloWorld')">Home</a>
      <a href="/#/docs" v-bind:class="isActive('Docs')">Docs</a>
      <a href="/#/contact" v-bind:class="isActive('Contact')">Contato</a>
    </div>
  </div>
</template>

<script>
export default {
  name: 'Header',
  methods: {
    isActive(page) {
      return this.$route.name === page ? 'active' : '';
    },
  },
};
</script>

<style>
  .logo {
    width: 2rem;
    margin: auto 2rem;
  }

  .header {
    display: flex;
    justify-content: baseline;
    align-items: center;

    padding: 2rem;
    margin-bottom: 3rem;
    border-bottom: 3px solid #41b883;
  }

  .nav a {
    text-decoration: none;
    color: #35495e;
    margin: auto 1rem;
    font-size: .8rem;
  }

  .nav a.active {
    color: #41b883;
    font-weight: bold;
  }
</style>
