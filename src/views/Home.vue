<template>
 <div id="nav">
    <router-link to="/admin">Home</router-link> |
    <router-link to="/about">About</router-link>
  </div>
   <router-view/>
</template>

<script>
// @ is an alias to /src

export default {
  name: 'Home',
}
</script>
<style lang='scss'>
#nav {
  padding: 30px;

  a {
    font-weight: bold;
    color: #2c3e50;

    &.router-link-exact-active {
      color: #42b983;
    }
  }
}
</style>
