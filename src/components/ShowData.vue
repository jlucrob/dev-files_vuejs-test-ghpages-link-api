<template>
  <div id="show-data">
    <h1>Usernames from test-rest-api on Heroku</h1>
    <div>
      <li v-for="item in data">{{item.username}}</li>
    </div>
  </div>
</template>

<script>
import axios from 'axios'

export default {
  name: 'show-data',
  data () {
    return {
      data: []
    }
  },
  created(){
    axios.get('https://enigmatic-atoll-46436.herokuapp.com/users')
    .then(result => {
      console.log(result.data);
      this.data = result.data;
    });
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
  margin: 10px 10px;
  list-style: none;
}
a {
  color: #42b983;
}
</style>
