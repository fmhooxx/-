<template>
  <div>
    <div>
    </div>
    <figure id="blinds-window">
      <div class="first"
           :class="current == 1? 'current1':''">
        <img @mouseenter="enter(1)"
             @mouseleave="leave(1)"
             src="../../assets/img/001.jpg"
             alt="" />
      </div>
      <div class="first"
           :class="current == 2? 'current1':''">
        <img @mouseenter="enter(2)"
             @mouseleave="leave(2)"
             src="../../assets/img/001.jpg"
             alt="" />
      </div>
      <div class="first"
           :class="current == 3? 'current1':''">
        <img @mouseenter="enter(3)"
             @mouseleave="leave(3)"
             src="../../assets/img/001.jpg"
             alt="" />
      </div>
      <div class="first"
           :class="current == 4? 'current1':''">
        <img @mouseenter="enter(4)"
             @mouseleave="leave(4)"
             src="../../assets/img/001.jpg"
             alt="" />
      </div>
      <div class="first"
           :class="current == 5? 'current1':''">
        <img @mouseenter="enter(5)"
             @mouseleave="leave(5)"
             src="../../assets/img/001.jpg"
             alt="" />
      </div>
      <div class="first"
           :class="current == 6? 'current1':''">
        <img @mouseenter="enter(6)"
             @mouseleave="leave(6)"
             src="../../assets/img/001.jpg"
             alt="" />
      </div>
    </figure>
  </div>
</template>

<script>

export default {
  name: 'Home',
  data () {
    return {
      current: 0
    }
  },
  methods: {
    enter (val) {
      this.current = val
    },
    leave (val) {
      this.current = 0
    }
  },
}
</script>

<style scoped>
figure {
  margin: 0 auto;
  position: relative;
  height: 600px;
  /* perspective: 1800px; */
  transform-style: preserve-3d;
  /* max-width: 1000px; */
  /* padding-bottom: 56.25%; */
  /* width: 100%; */
  /* height: 100%; */
}
figure div {
  top: 0;
  left: 0;
  position: absolute;
  transition: 1s;
  width: 100%;
  height: 100%;
}
.first span {
  position: absolute;
}
figure div.first {
  transform: rotateY(0deg);
}
.current1 {
  transform: rotateY(180deg) !important;
}
figure div:nth-child(1) {
  clip: rect(0px, 100px, 840px, 0px);
  transform-origin: 50px 0px;
}
figure div:nth-child(2) {
  clip: rect(0px, 200px, 840px, 100px);
  transform-origin: 150px 0px;
  transition-delay: 100ms;
}
figure div:nth-child(3) {
  clip: rect(0px, 300px, 840px, 200px);
  transform-origin: 250px 0px;
  transition-delay: 200ms;
}
figure div:nth-child(4) {
  clip: rect(0px, 400px, 840px, 300px);
  transform-origin: 350px 0px;
  transition-delay: 300ms;
}
figure div:nth-child(5) {
  clip: rect(0px, 500px, 840px, 400px);
  transform-origin: 450px 0px;
  transition-delay: 400ms;
}
figure div:nth-child(6) {
  clip: rect(0px, 600px, 840px, 500px);
  transform-origin: 550px 0px;
  transition-delay: 500ms;
}
/* figure:hover div.first {
  transform: rotateY(180deg);
} */
/* figure div:nth-child(1) {
  clip: rect(0px, 300px, 1200px, -200px);
  transform-origin: 150px 0px;
}
figure div:nth-child(2) {
  clip: rect(0px, 500px, 1200px, 100px);
  transform-origin: 350px 0px;
  transition-delay: 100ms;
}
figure div:nth-child(3) {
  clip: rect(0px, 600px, 1200px, 300px);
  transform-origin: 450px 0px;
  transition-delay: 200ms;
}
figure div:nth-child(4) {
  clip: rect(0px, 700px, 1200px, 500px);
  transform-origin: 500px 0px;
  transition-delay: 300ms;
}
figure div:nth-child(5) {
  clip: rect(0px, 800px, 1200px, 700px);
  transform-origin: 650px 0px;
  transition-delay: 400ms;
}
figure div:nth-child(6) {
  clip: rect(0px, 900px, 1200px, 900px);
  transform-origin: 750px 0px;
  transition-delay: 500ms;
} */
</style>