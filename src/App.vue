  <template>
    <div id="app">
    <button @click="loadData">click me</button>
      <data-tables :data="gridData"></data-tables>
    </div>
  </template>

  <script>
  import Hello from './components/Hello'
  import DataTables from './components/DataTables'
  

  export default {
    name: 'app',
    mounted(){
      this.loadData();      
    },
    data(){
      return{
        gridData:[],
      }
    },
    methods:{
      loadData:function(){
                          var url = "http://cnodejs.org/api/v1/topics";
                          var httpOptions = {
                                     
                          };
                          this.$http.get(url, httpOptions).then(function (response) {
                              // 响应成功回调
                              var json_data=response.data.data;
                                this.$set(this.gridData, JSON.stringify(json_data));
                               //console.log(json_data);
                              // return json_data;
                          },
                          function (response) {
                              // 响应错误回调
                              alert('访问失败', '错误');
                          }
                          );
                          //this.$broadcast('init', this.gridData)
                      },
    },
    components: {
      Hello,DataTables
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
