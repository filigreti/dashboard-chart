<template>
  <div class="d-flex" id="app">
    <div id="nav">
      <Sidebar />
    </div>
    <div class="route-area">
      <TopHeader class="t-header" />
      <div class="router-container">
        <router-view />
      </div>
    </div>
  </div>
</template>

<script>
import Sidebar from './components/Sidebar';
import TopHeader from './components/TopHeader';
export default {
  components: {
    Sidebar,
    TopHeader
  }
};
</script>

<style>
* {
  box-sizing: border-box;
}
body {
  margin: 0;
  padding: 0;
}
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
}

#nav {
  width: 243px;
  height: 100vh;
  position: sticky;
  top: 0;
  background: #18335a;
}

#nav a {
  font-weight: bold;
  color: white;
  text-decoration: none;
}

#nav a.router-link-exact-active {
  color: white;
  text-decoration: none;
  border-radius: 4px;
  background-color: #0093dd;
}
.route-area {
  flex: 1;
  background: #fcfcfd;
}
.t-header {
  height: 68px;
  box-shadow: 0 7px 64px 0 rgba(19, 36, 78, 0.07);
  background-color: #ffffff;
  padding: 0 42px;
  position: sticky;
  top: 0;
}
.router-container {
  padding: 40px 40px 0 42px;
}
</style>
