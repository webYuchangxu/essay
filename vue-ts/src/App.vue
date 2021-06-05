<template>
  <div id="app">
    <!-- <img alt="Vue logo" src="./assets/logo.png" />
    <HelloWorld msg="Welcome to Your Vue.js + TypeScript App" /> -->
    <component :is="componentId"></component>
    <BackToTop></BackToTop>
  </div>
</template>

<script lang="ts">
import { Component, Vue } from "vue-property-decorator";
import HelloWorld from "./components/HelloWorld.vue";
import Home from "./components/Home.vue";
import BackToTop from "./components/BackToTop.vue";

@Component({
  components: {
    HelloWorld,
    Home,
    BackToTop,
  },
})
export default class App extends Vue {
  // eslint-disable-next-line
  public componentId: any = "";
  created(): void {
    this.componentId = Home;
  }
}
</script>

<style lang="less">
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
}
</style>
