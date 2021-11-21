<template>
  <div id="app">



    <div id="nav">
      <router-link to="/">Home</router-link> |
      <router-link to="/artists">Artists</router-link> |
      <router-link to="/Showcase">Portrayed</router-link> |
      <router-link to="/Statistics">Statistics</router-link> |
      <router-link to="/Blog">Blog</router-link> |
      <router-link to="/about">About</router-link>
    </div>
    <router-view/>
  </div>
</template>







<style lang="scss">



#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  color: #2c3e50;
}

#nav {
  padding: 30px;
  text-align: center;
  font-size: 2em;

  a {
    font-weight: bold;

    color: #2c3e50;

    &.router-link-exact-active {
      color: #ff0000;
    }
  }
}
</style>
