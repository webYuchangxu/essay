<template>
  <div class="bg"></div>
</template>
<script lang="ts">
import { Component, Vue } from "vue-property-decorator";

@Component({
  components: {},
})
export default class Home extends Vue {}
</script>
<style lang="less">
.bg {
  height: 200vh;
  background: url(../assets/bg.jpeg) center top;
}
</style>
