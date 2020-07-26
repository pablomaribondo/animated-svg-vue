<template>
  <div id="app">
    <h1>Animated SVG Vue Component</h1>
    <input type="range" min="0" max="4" step="1" v-model="index" />
    <SVGCanvas :current-index="index" :animation-data="animationData" />
  </div>
</template>

<script>
import { Back } from 'gsap';
import SVGCanvas from './components/SVGCanvas.vue';

export default {
  name: 'App',
  components: {
    SVGCanvas,
  },
  data() {
    return {
      index: 0,
      animationData: {
        svgID: '#lifestyle',
        frames: [{
          name: 'frame1',
          objects: [{
            id: 'frame1-poles',
            set: {
              scaleY: 0, x: 190, y: 75, transformOrigin: '50% 100%',
            },
            animate: { alpha: 1, scaleY: 1, ease: Back.easeOut },
          },
          {
            id: 'hammock',
            set: {
              scale: 0.5, x: 220, y: 110, transformOrigin: '50% 100%',
            },
            animate: {
              alpha: 1, scale: 1, delay: 0.1, ease: Back.easeOut,
            },
          },
          ],
        },
        {
          name: 'frame2',
          objects: [{
            id: 'frame2-poles',
            set: {
              scaleY: 0, x: 160, y: 15, transformOrigin: '50% 100%',
            },
            animate: { alpha: 1, scaleY: 1, ease: Back.easeOut },
          },
          {
            id: 'hammock',
            set: {
              scale: 0.5, x: 220, y: 110, transformOrigin: '50% 100%',
            },
            animate: {
              alpha: 1, scale: 1, delay: 0.1, ease: Back.easeOut,
            },
          },
          ],
        },
        {
          name: 'frame3',
          objects: [{
            id: 'frame2-poles',
            set: {
              scaleY: 0, x: 160, y: 15, transformOrigin: '50% 100%',
            },
            animate: { alpha: 1, scaleY: 1, ease: Back.easeOut },
          },
          {
            id: 'hammock',
            set: {
              scale: 0.5, x: 220, y: 110, transformOrigin: '50% 100%',
            },
            animate: {
              alpha: 1, scale: 1, delay: 0.1, ease: Back.easeOut,
            },
          },
          {
            id: 'bbq',
            set: {
              scale: 0.5, x: 120, y: 110, transformOrigin: '50% 100%',
            },
            animate: {
              alpha: 1, scale: 1, delay: 0.3, ease: Back.easeOut,
            },
          },
          {
            id: 'floor1',
            set: {
              scale: 0.5, x: 90, y: 250, transformOrigin: '50% 100%',
            },
            animate: {
              alpha: 1, scale: 1, delay: 0.2, ease: Back.easeOut,
            },
          },
          ],
        },
        {
          name: 'frame4',
          objects: [{
            id: 'frame3-poles',
            set: {
              scaleY: 0, scaleX: 0.94, x: 155, y: 15, transformOrigin: '50% 100%',
            },
            animate: { alpha: 1, scaleY: 1, ease: Back.easeOut },
          },
          {
            id: 'hammock',
            set: {
              scale: 0.5, x: 220, y: 110, transformOrigin: '225px 100px',
            },
            animate: {
              alpha: 1, scale: 1, rotation: 0, delay: 0.1, ease: Back.easeOut,
            },
          },
          {
            id: 'bbq',
            set: {
              scale: 0.5, x: 120, y: 110, transformOrigin: '45px 210px',
            },
            animate: {
              alpha: 1, scale: 1, delay: 0.3, ease: Back.easeOut,
            },
          },
          {
            id: 'tree',
            set: {
              scale: 0.5, x: 340, y: 20, transformOrigin: '20px 200px',
            },
            animate: {
              alpha: 1, scale: 1, delay: 0.4, ease: Back.easeOut,
            },
          },
          {
            id: 'floor2',
            set: {
              scale: 0.5, x: 90, y: 250, transformOrigin: '50% 100%',
            },
            animate: {
              alpha: 1, scale: 1, delay: 0.2, ease: Back.easeOut,
            },
          },
          {
            id: 'man',
            set: {
              scale: 0.5, x: 212, y: 180, transformOrigin: '20px 200px',
            },
            animate: {
              alpha: 1, scale: 1, delay: 0.5, ease: Back.easeOut,
            },
          },
          ],
        },
        {
          name: 'frame5',
          objects: [{
            id: 'frame3-poles',
            set: {
              scaleY: 0, scaleX: 0.94, x: 155, y: 15, transformOrigin: '50% 100%',
            },
            animate: { alpha: 1, scaleY: 1, ease: Back.easeOut },
          },
          {
            id: 'hammock',
            set: {
              scale: 0.5, rotation: -10, x: 220, y: 110, transformOrigin: '225px 100px',
            },
            animate: {
              alpha: 1, scale: 1, rotation: 0, delay: 0.1, ease: Back.easeOut,
            },
          },
          {
            id: 'bbq',
            set: {
              scale: 0.5, x: 120, y: 110, transformOrigin: '45px 210px',
            },
            animate: {
              alpha: 1, scale: 1, delay: 0.3, ease: Back.easeOut,
            },
          },
          {
            id: 'tree',
            set: {
              scale: 0.5, x: 340, y: 20, transformOrigin: '20px 200px',
            },
            animate: {
              alpha: 1, scale: 1, delay: 0.4, ease: Back.easeOut,
            },
          },
          {
            id: 'floor3',
            set: {
              scale: 0.5, x: 90, y: 250, transformOrigin: '50% 100%',
            },
            animate: {
              alpha: 1, scale: 1, delay: 0.2, ease: Back.easeOut,
            },
          },
          {
            id: 'man',
            set: {
              scale: 0.5, x: 212, y: 180, transformOrigin: '20px 200px',
            },
            animate: {
              alpha: 1, scale: 1, delay: 0.5, ease: Back.easeOut,
            },
          },
          {
            id: 'stove',
            set: {
              scale: 0.5, x: 190, y: 270, transformOrigin: '200px 200px',
            },
            animate: {
              alpha: 1, scale: 1, delay: 0.3, ease: Back.easeOut,
            },
          },
          {
            id: 'umbrella',
            set: {
              scale: 0.5, x: 240, y: 100, transformOrigin: '80px 160px',
            },
            animate: {
              alpha: 1, scale: 1, delay: 0.3, ease: Back.easeOut,
            },
          },
          ],
        },
        ],
      },
    };
  },
};
</script>

<style lang="scss">
body, html {
  background: #CCCCCC;
  font-family: 'Patua One', cursive;
  font-size: 26px;
  color: white;
  letter-spacing: 1px;
  padding: 0;
  margin: 0;
  overflow: hidden;
}

#app {
  position: relative;
  width: 600px;
  margin: 50px auto;
}

h1 {
  font-size: 42px;
  text-align: center;
  margin-bottom: 10px;
  margin-top: 0;
}

input[type=range] {
 width: 60%;
 margin-left: 20%;
 margin-top: 20px;
}
</style>
