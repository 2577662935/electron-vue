<template>
  <div id="wrapper">
    <main>
      <div class="left-side">
        <span class="title">
          Welcome to your new project!
        </span>
        <el-button type="primary">主要按钮</el-button>
        <el-button type="primary" icon="el-icon-search">搜索</el-button>
        <el-button type="primary">上传<i class="el-icon-upload el-icon--right"></i></el-button>
        <system-information></system-information>
      </div>
    </main>
  </div>
</template>

<script>
  import SystemInformation from './LandingPage/SystemInformation'
  export default {
    name: 'landing-page',
    components: { SystemInformation },
    methods: {
      open (link) {
        this.$electron.shell.openExternal(link)
      }
    },
    mounted () {
      console.log(11111)
    }
  }
</script>

<style>
  * {
    box-sizing: border-box;
    margin: 0;
    padding: 0;
  }

  body {
    font-family: 'Source Sans Pro', sans-serif;
    background-color: #ffffff;
  }

  #wrapper {
    height: 100vh;
    padding: 60px 80px;
    width: 100vw;
  }
  .left-side{
    /*background-color: red;*/
  }
</style>
