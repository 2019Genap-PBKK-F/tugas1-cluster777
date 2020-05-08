<template>
    <div>The component will appear here</div>
</template>
<script>
import axios from 'axios'
var host = 'http://127.0.0.1:8009/'

import WebDataRocks from 'webdatarocks'
export default {
  mounted: function() {
    axios.get(host + 'api/penelitian/').then(res => {
      console.log(res.data)
      this.webdatarocks = new WebDataRocks({
        report: { data: res.data },
        container: this.$el
      })
    })
  },
  beforeUpdate() {
    return false
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
@import '~webdatarocks/webdatarocks.min.css';
</style>
