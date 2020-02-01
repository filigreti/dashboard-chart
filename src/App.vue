<template>
  <div class="d-flex" id="app">
    <div class="nav-side" ref="nav" :style="`width:${size}px; `">
      <Sidebar v-if="!change" />
      <Smallbar v-else />
    </div>
    <div :style="`margin-left:${widthArea}px`" ref="routeCont" class="route-area">
      <TopHeader v-model="change" class="t-header" />
      <div class="router-container">
        <router-view />
      </div>
    </div>
  </div>
</template>

<script>
import Sidebar from "./components/Sidebar";
import Smallbar from "./components/Smallbar";
import TopHeader from "./components/TopHeader";
export default {
  data() {
    return {
      sidebar: "",
      size: 243,
      change: false
    };
  },
  components: {
    Sidebar,
    TopHeader,
    Smallbar
  },
  watch: {
    change(x) {
      if (x == true) {
        this.size = 68;
        this.sidebar = 68;
      } else {
        this.size = 243;
        this.sidebar = 243;
      }
    }
  },
  computed: {
    widthArea() {
      return this.sidebar;
    }
  },
  mounted() {
    this.sidebar = this.$refs.nav.clientWidth;
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
html {
  font-size: 16px;
}
#app {
  font-family: "Avenir", Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
}

.nav-side {
  position: fixed;
  left: 0;
  min-height: 100vh;
  background: #18335a;
  overflow: hidden;
}

.nav-side a,
.nav-side a:hover {
  font-weight: bold;
  color: white;
  text-decoration: none !important;
}

.nav-side a.router-link-exact-active {
  color: white;
  text-decoration: none;
  border-radius: 4px;
  background-color: #0093dd;
}

.route-area {
  flex: 1;
  background: #fcfcfd;
  box-sizing: border-box;
  /* margin-left: 243px; */
}
.t-header {
  height: 68px;
  box-shadow: 0 7px 64px 0 rgba(19, 36, 78, 0.07);
  background-color: #ffffff;
  padding: 0 42px;
  position: sticky;
  top: 0;
  z-index: 10;
}
.router-container {
  padding: 40px 40px 0 42px;
  box-sizing: border-box;
}
.component-fade-enter-active,
.component-fade-leave-active {
  transition: opacity 0.3s ease;
}
.component-fade-enter, .component-fade-leave-to
/* .component-fade-leave-active below version 2.1.8 */ {
  opacity: 0;
}
</style>
