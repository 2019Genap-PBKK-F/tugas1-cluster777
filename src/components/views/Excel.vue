<template lang="html">
  <div class="wrapper-jexcel">
    
    <input
      type='button'
      value='Add new row'
      @click='jExcelObj.insertRow()'
    /><br />
    <div id='spreadsheet' ref='spreadsheet'></div>
  </div>
</template>
<?php

$host = "localhost"; /* Host name */
$user = "root"; /* User */
$password = ""; /* Password */
$dbname = "coba"; /* Database name */

$con = mysqli_connect($host, $user, $password,$dbname);
// Check connection
if (!$con) {
  die("Connection failed: " . mysqli_connect_error());
}
?>
<script>
import jexcelStyle from 'jexcel/dist/jexcel.css' // eslint-disable-line no-unused-vars
import jexcel from 'jexcel' // eslint-disable-line no-unused-vars

export default {
  name: 'jexcel',
  data() {
    return {
      myCars: [
[ '0511140000089', 'a', '11-07-2009', '', '2014', true ],
[ '0511140000039', 'b', '08-05-2009', '', '2014', true ],
[ '0511140000029', 'c', '17-02-09', '', '2014', true ],
[ '0511140000019', 'd', '22-02-09', '', '2014', false ],
[ '0511140000009', 'e', '03-01-09', '', '2014', true ],
[ '0511140000119', 'f', '25-10-09', '', '2014', true ]
      ]
    }
  },
  computed: {
    jExcelOptions() {
      return {
        data: this.myCars,
        columns: [
{ type: 'text', title: 'nrp', width: '120px' },
{ type: 'text', title: 'nama', width: '120px' },
{ type: 'calendar', title: 'tanggal lahir', width: '120px' },
{ type: 'image', title: 'photo', width: '120px' },
{ type: 'text', title: 'angkatan', width: '120px' },
{ type: 'checkbox', title: 'aktif', width: '120px' }
        ]
      }
    }
  },
  methods: {
    insertRowc() {
      console.log(this)
      // this.spreadsheet.insertRow()
    }
  },
  mounted: function() {
    // console.log(this.jExcelOptions)
    // console.log(this.$refs['spreadsheet'])
    const jExcelObj = jexcel(this.$refs['spreadsheet'], this.jExcelOptions)
    // Object.assign(this, jExcelObj) // pollutes component instance
    Object.assign(this, { jExcelObj }) // tucks all methods under jExcelObj object in component instance
    // console.log(this.jExcelObj)
  }
}

</script>

<style lang='css' scoped>
.introduction {
  font-size: 14px;
  padding: 0.5em;
  margin-bottom: 0.3em;
  color: gold;
  background: #111;
}
</style>
