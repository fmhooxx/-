<template>
  <div>
    <div class="box">
      <div class="one"
           :class="current == 1 ? 'mouseenter':''"
           @mouseenter="enter(1)"
           @mouseleave="leave(1)">1</div>
      <div class="two"
           :class="current == 2 ? 'mouseenter':''"
           @mouseenter="enter(2)"
           @mouseleave="leave(2)">2</div>
      <div class="three"
           :class="current == 3 ? 'mouseenter':''"
           @mouseenter="enter(3)"
           @mouseleave="leave(3)">3</div>
      <div class="four"
           :class="current == 4 ? 'mouseenter':''"
           @mouseenter="enter(4)"
           @mouseleave="leave(4)">4</div>
      <div class="five"
           :class="current == 5 ? 'mouseenter':''"
           @mouseenter="enter(5)"
           @mouseleave="leave(5)">5</div>
      <div class="six"
           :class="current == 6 ? 'mouseenter':''"
           @mouseenter="enter(6)"
           @mouseleave="leave(6)">6</div>
      <!-- <div v-for="(item, index) in list"
           :key="index"
           @mouseenter="enter(index)"
           @mouseleave="leave()">{{item.text}}</div> -->
    </div>
  </div>
</template>

<script>

export default {
  name: 'Home',
  data () {
    return {
      list: [
        {
          text: 1
        },
        {
          text: 2
        },
        {
          text: 3
        },
        {
          text: 4
        },
        {
          text: 5
        },
        {
          text: 6
        },
      ],
      current: 0
    }
  },
  methods: {
    enter (val) {
      this.current = val
    },
    leave () {
      this.current = 0
    }
  },
}
</script>

<style lang="sass" scoped>
.box
  display: flex
  justify-content: space-evenly
  height: 600px
  > div
    height: 100%
    width: 100%
    @keyframes move
      0%
        width: 0
      100%
        width: 100%

  .one
    background-color: rgb(214, 90, 90)
    align-self: flex-start
    animation: move 6s linear forwards

  .two
    background-color: rgb(90, 214, 117)
    animation: move 6s linear forwards

  .three
    background-color: rgb(90, 179, 214)
    animation: move 6s linear forwards

  .four
    background-color: rgb(131, 38, 66)
    animation: move 6s linear forwards

  .five
    background-color: rgb(109, 90, 214)
    animation: move 6s linear forwards

  .six
    background-color: rgb(128, 38, 131)
    animation: move 6s linear forwards

  .mouseenter
    animation: mouseenterMove 6s linear forwards
  @keyframes mouseenterMove
    0%
      transform: rotate(45deg)
      background-color: #fff

    12.5% 
      transform: rotate(90deg)

    25%
      transform: rotate(135deg)

    37.5% 
      transform: rotate(180deg)

    50%
      transform: rotate(225deg)

    62.5% 
      transform: rotate(270deg)

    75%
      transform: rotate(315deg)

    100%
      transform: rotate(360deg)
</style>