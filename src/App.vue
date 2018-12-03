<template>
  <div id="app">
    <iframe width="100%" height="500" scrolling="no"
    :src="`${baseUrl}web/viewer.html?file=${baseUrl}web/compressed.tracemonkey-pldi-09.pdf`"></iframe>
  </div>
</template>

<script>
import HelloWorld from './components/HelloWorld.vue'
// 如果是用vue-cli2生成的项目,需要将文件复制到static目录下去,然后在template引入:
/**
 * <iframe v-show="pdf.showPDF"
        width="100%" height="500" scrolling="no"
        :src='"/static/web/viewer.html?file=" + pdf.pageUrl'></iframe>
 */
export default {
  name: 'app',
  components: {
    HelloWorld
  },
  data () {
    return {
      baseUrl: process.env.BASE_URL
    }
  }
}
</script>

<style>
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
