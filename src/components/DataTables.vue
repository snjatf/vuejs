<template>  
  <div class="datatables">
    <table>
    <th>
    <td v-for="col in columns">col.text</td>
    </th>

    </table>
  </div>
</template>

<script>
export default {
  name: 'datatables',
  props:['data'],
  data () {
    return {
      msg: 'Welcome to Your Vue.js <App13131>'
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h1, h2 {
  font-weight: normal;
}

ul {
  list-style-type: none;
  padding: 0;
}

li {
  display: inline-block;
  margin: 0 10px;
}

a {
  color: #42b983;
}
</style>
