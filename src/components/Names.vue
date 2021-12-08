<template>
<div class="container">
    <h3>Names:</h3>
    <table class="table">
      <thead>
        <tr>
          <th scope="col">activity</th>
          <th scope="col">type</th>
          <th scope="col">participants</th>
          <th scope="col">link</th>
          <th scope="col">key</th>
          <th scope="col">accessibility</th>
        </tr>
      </thead>
      <tbody>
        <tr> 
          <td>{{names.activity}}</td>
          <td>{{names.type}}</td>
          <td>{{names.participants}}</td>
          <td>{{names.link}}</td>
          <td>{{names.key}}</td>
          <td>{{names.accessibility}}</td>

        </tr>
      </tbody>
    </table> 
  </div> 
</template>

<!--{"activity":"Bake pastries for you and your neighbor",
"type":"cooking",
"participants":1,
"price":0.4,
"link":"",
"key":"8125168",
"accessibility":0.3}
-->

<script>
import axios from 'axios';

  export default {
    name: 'Names',
    data(){
        return {
            names: []
            };
  },
  created: function(){
      axios
      .get("http://www.boredapi.com/api/activity/")
      .then(res => {
          this.names = res.data;
          console.log(this.names)
          })
          }
          }
</script>



<style>
  h3 {
    margin-bottom: 5%;
  }
</style>