<template>
  <div>


    <div class="div-box" @mouseover="mouseOver">Mouse Over</div>
    <div class="div-box" @mouseleave="mouseLeave">Mouse Leave</div>
    <div class="div-box" @dblclick="dblClick">Double Clicked</div>
    <div class="div-box" @mousemove="mouseMove">Mouse Move -- {{ x + ' ' + y }}</div>


  </div>
</template>

<script>
export default {
  name: 'IndexPage',
  data(){
    return {
      x: 0,
      y: 0
    }
  },
  methods: {
    mouseOver(){
      alert('Mouse Over')
    },
    mouseLeave(){
      alert('Mouse Leave')
    },
    dblClick(){
      alert('Double Clicked')
    },
    mouseMove(e){
      this.x = e.offsetX
      this.y = e.offsetY
    }
  }
}
</script>

<style lang="scss" scoped>

.div-box{
  width: 300px;
  padding: 50px 0px;
  background-color: aqua;
  margin:20px;
}

</style>
