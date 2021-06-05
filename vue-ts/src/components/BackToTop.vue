<template>
  <div class="backToTop" @click="toTop"></div>
</template>
<script lang="ts">
import { Component, Vue } from "vue-property-decorator";

@Component({
  components: {},
})
export default class BackToTop extends Vue {
  toTop(): void {
    const step = {
      delay: 5,
      num: 10,
    };
    const timer = setInterval(() => {
      let height = document.documentElement.scrollTop - step.num;
      document.body.scrollTop = document.documentElement.scrollTop = height;
      if (height < 0) {
        clearInterval(timer);
      }
    }, step.delay);
  }
}
</script>
<style lang="less">
.backToTop {
  position: fixed;
  bottom: 40px;
  right: 40px;
  height: 40px;
  width: 40px;
  background-size: contain;
  background-image: url(../assets/top.svg);
  opacity: 0.5;
}
.backToTop:hover {
  opacity: 1;
  box-shadow: 0 0 20px 1px #ffffff inset, 0 0 2px 1px #fff;
  border-radius: 5px;
}
</style>
