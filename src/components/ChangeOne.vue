<template>
  <div class="container_one">

    <h5 style="margin-top:50px">子组件一</h5>
    <el-button @click="btnClick01" type="primary" style="margin-top:50px">切换颜色按钮</el-button>

  </div>
</template>

<script>
  export default {
    props: {
      cl01: String
    },
    data() {
      return {
        cl02: ''
      }
    },
    //生命周期 - 创建完成（访问当前this实例）
    created() {

    },
    //生命周期 - 挂载完成（访问DOM元素）
    mounted() {

    },
    methods: {
      btnClick01() {
        this.cl02 = 'blue'
        this.$emit('colorDate', this.cl02)
      }
    }
  }

</script>
<style>
  .container_one {
    width: 200px;
    height: 250px;
    border: 1px solid #5D8FD6;
    text-align: center;
    background: #DAE8FC;
  }

</style>
