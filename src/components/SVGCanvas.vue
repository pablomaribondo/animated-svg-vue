<template>
  <div class="svgcanvas">
    <svg class>
      <use :xlink:href="animationData.svgID" />
    </svg>
    <InlineSVG />
  </div>
</template>

<script>
import { TweenMax, Expo } from 'gsap';

import InlineSVG from './InlineSVG.vue';

export default {
  name: 'SVGCanvas',
  components: {
    InlineSVG,
  },
  props: ['animationData', 'currentIndex'],
  watch: {
    currentIndex() {
      this.updateFrame();
    },
  },
  methods: {
    updateFrame() {
      TweenMax.killAll();
      const frameObjects = this.animationData.frames[this.currentIndex].objects;
      TweenMax.set('.svg-object', { alpha: 0, ease: Expo.easeOut });

      for (let i = 0; i < frameObjects.length; i += 1) {
        TweenMax.set(`#${frameObjects[i].id}`, frameObjects[i].set);
        TweenMax.to(`#${frameObjects[i].id}`, 0.17, frameObjects[i].animate);
      }
    },
  },
  mounted() {
    this.updateFrame();
  },
};
</script>

<style scoped lang="scss">
.svgcanvas {
  width: 100%;
  height: 100%;
  margin-top: 0px;

  svg {
    width: 100%;
    height: 400px;
  }
}
</style>
