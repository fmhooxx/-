<template>
  <div>
    <div class="hello">
      <div class="con"
           :class="[current == 1 ? 'mouseenter':'',leaveCurrent == 11 ? 'mouseenterLeave':'']"
           @mouseenter="enter(1)"
           @mouseleave="leave(1)">
        <div class="one">1</div>
      </div>
      <div class="con"
           :class="[current == 2 ? 'mouseenter':'',leaveCurrent == 12 ? 'mouseenterLeave':'']"
           @mouseenter="enter(2)"
           @mouseleave="leave(2)">
        <div class="two">2</div>
      </div>
      <div class="con"
           :class="[current == 3 ? 'mouseenter':'',leaveCurrent == 13 ? 'mouseenterLeave':'']"
           @mouseenter="enter(3)"
           @mouseleave="leave(3)">
        <div class="three">3</div>
      </div>
      <div class="con"
           :class="[current == 4 ? 'mouseenter':'',leaveCurrent == 14 ? 'mouseenterLeave':'']"
           @mouseenter="enter(4)"
           @mouseleave="leave(4)">
        <div class="four">4</div>
      </div>
      <div class="con"
           :class="[current == 5 ? 'mouseenter':'',leaveCurrent == 15 ? 'mouseenterLeave':'']"
           @mouseenter="enter(5)"
           @mouseleave="leave(5)">
        <div class="five">5</div>
      </div>
      <div class="con"
           :class="[current == 6 ? 'mouseenter':'',leaveCurrent == 16 ? 'mouseenterLeave':'']"
           @mouseenter="enter(6)"
           @mouseleave="leave(6)">
        <div class="six">6</div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  data () {
    return {
      current: 0,
      leaveCurrent: 0,
    }
  },
  methods: {
    enter (val) {
      this.current = val
    },
    leave (val) {
      this.current = 0
      if (val == 1) {
        this.leaveCurrent = 11
      } else if (val == 2) {
        this.leaveCurrent = 12
      } else if (val == 3) {
        this.leaveCurrent = 13
      } else if (val == 4) {
        this.leaveCurrent = 14
      } else if (val == 5) {
        this.leaveCurrent = 15
      } else if (val == 6) {
        this.leaveCurrent = 16
      }
    }
  },
}
</script>
<style scoped>
.hello {
  /* padding: 10px; */
  height: 100vh;
  /* height: 100%; */
  /* padding: 50px; */
  /* perspective: 1000px; */
}
.con {
  display: inline-flex;
  width: 16.66%;
  position: relative;
  height: 100%;
}
.con div {
  width: 0;
  height: 100%;
  position: absolute;
  top: 0;
  left: 0;
  display: flex;
  justify-content: center;
  align-items: center;
  overflow: hidden;
  color: #fff;
  font-size: 36px;
  font-style: italic;
  /* background: lightpink; */
  animation: move 0.6s linear forwards;
  background-repeat: no-repeat;
  background-size: 100% 100%;
}
.one {
  background: url("../../assets/img/1_01.jpg");
}
.two {
  background: url("../../assets/img/1_02.png");
}
.three {
  background: url("../../assets/img/1_03.png");
}
.four {
  background: url("../../assets/img/1_04.png");
}
.five {
  background: url("../../assets/img/1_05.png");
}
.six {
  background: url("../../assets/img/1_06.png");
}
.mouseenterLeave {
  animation: flipLeave 0.5s linear forwards;
}
@keyframes flipLeave {
  0% {
    transform: rotateY(60deg);
  }
  25% {
    transform: rotateY(45deg);
  }
  50% {
    transform: rotateY(30deg);
  }
  75% {
    transform: rotateY(15deg);
  }
  100% {
    transform: rotateY(0);
  }
}
.mouseenter {
  /* animation: mouseenterMove 6s linear forwards; */
  animation: flip 0.5s linear forwards;
}
@keyframes flip {
  0% {
    transform: rotateY(0);
  }
  25% {
    transform: rotateY(15deg);
  }
  50% {
    transform: rotateY(30deg);
  }
  75% {
    transform: rotateY(45deg);
  }
  100% {
    transform: rotateY(60deg);
  }
}
@keyframes mouseenterMove {
  0% {
    transform: rotate(0deg) scale(1);
  }

  12.5% {
    transform: rotate(45deg) scale(1.2);
  }
  25% {
    transform: rotate(90deg) scale(1.4);
  }

  37.5% {
    transform: rotate(135deg) scale(1.6);
  }
  50% {
    transform: rotate(180deg) scale(1.8);
  }

  62.5% {
    transform: rotate(225deg) scale(1.6);
  }

  75% {
    transform: rotate(270deg) scale(1.4);
  }
  87.5% {
    transform: rotate(315deg) scale(1.2);
  }

  100% {
    transform: rotate(360deg) scale(1);
  }
}
@keyframes move {
  0% {
    width: 0;
  }
  100% {
    width: 100%;
  }
}
</style>