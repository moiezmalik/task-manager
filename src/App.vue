<template>
  <div id="nav">
    <nav>
    <router-link to="/">Home</router-link> |
    <router-link to="/about">About</router-link>
    </nav>
  </div>
  <router-view/>
  <Footer />
</template>

<script>
import Footer from './components/footer.vue'
export default {
  name: 'App',
  components: {
    Footer,
  }
}
</script>

<style>
h1{
  font-size: 24px;
}
h2{
  font-size: 20px;
}
h3{
  font-size: 18px;
}
h4{
  font-size: 18px;
}
p{
  font-size: 16px;
}
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  color: #2c3e50;
}

#nav {
  padding: 30px;
  text-align: center;
}

#nav a {
  font-weight: bold;
  color: #2c3e50;
}

#nav a.router-link-exact-active {
  color: #42b983;
}
</style>
