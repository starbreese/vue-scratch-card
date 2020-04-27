<template>
  <div id="app">
    <vue-scratch-card 
        element-id='scratchWrap'
        :ratio=0.5
        :move-radius=50
        :start-callback=startCallback
        :clear-callback=clearCallback
    />
  </div>
</template>

<script>
export default {
    name: 'app',
    data () {
        return {
            msg: 'Welcome to Your Vue.js App'
        };
    },
    methods : {
        startCallback(){
            console.log('抽奖成功！');
        },
        clearCallback(){
            console.log('清除完毕！');
        }
    }
};
</script>

<style lang="scss">
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
