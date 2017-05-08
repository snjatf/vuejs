  <template>  
    <div class="datatables">
      <table>
      <tbody>
      <tr v-for="item in data">
        <td>{{item.id}}</td>
      </tr>
      </tbody>
      </table>
    </div>
  </template>

  <script>
  export default {
    name: 'datatables',
    props: {
      data: {
        type: Array,
        required: true
      }
      },
      mounted(){
        //console.log("1");
        var x=this.data;
        console.log(x);
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
