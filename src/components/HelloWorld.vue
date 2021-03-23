<template>
  <div class="container" :style="{background:cl01}">
    <div class="container_btn">
      <el-button @click="switchColor()" type="success">颜色切换按钮</el-button>
      <el-button @click="getColor()">显示颜色按钮</el-button>
    </div>

    <div style="display: flex;
    justify-content: space-around;margin-top:30px">
      <Chone @colorDate="cpnClick"></Chone>
      <ChTwo @colorDate="cpnClick"></ChTwo>
    </div>

  </div>
</template>

<script>
  import Chone from './ChangeOne.vue'
  import ChTwo from './ChangeTwo.vue'
  export default {
    components: {
      Chone,
      ChTwo
    },
    name: 'HelloWorld',
    data() {
      return {
        cl01: '',
      }
    },
    methods: {
      getColor() {
        alert(this.cl01)
      },
      switchColor() {
        this.cl01 = 'green'
      },
      //父组件中定义方法来接收子组件传的值
      cpnClick(item) {
        this.cl01 = item
      }

    }
  }

</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style>
  * {
    padding: 0;
    margin: 0;
    box-sizing: border-box;
  }

  .container {
    width: 500px;
    height: 500px;
    background: #F5F5F5;
    margin: 0 auto;
    margin-top: 20px;
    overflow: hidden;
  }

  .container_btn {
    width: 100%;
    display: flex;
    justify-content: space-around;
    margin-top: 20px;
  }

</style>
