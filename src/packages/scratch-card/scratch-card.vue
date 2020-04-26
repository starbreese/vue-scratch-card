<template>
  <div :id="elementId" class="scratchCard">
    <div class="result" v-show='showLucky'>
      <slot name="result"></slot>
      <img :src="resultImg" alt="" class="pic"/>
    </div>
    <canvas id="scratchCanvas"></canvas>
  </div>
</template>
<script>
export default {
  name: 'vueScratchCard'

}
</script>
<style lang='scss'>
  .scratchCard{
      position: relative;
      width:90%;
      height:40vw;
      margin:0 auto;
      .result{
          position: absolute;
          width:100%;
          height:100%;
          top:0;
          left:0;
      }
      .pic{
          width:100%;
          height:100%;
      }
      canvas{
          position: relative;
          z-index: 2;
      }
  }
</style>