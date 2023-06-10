# single component create , methods, event

<template>
  <div>
    <h1> Hello From home Component </h1>
    <h2>{{ data }}</h2>
    <h2>{{ msg }}</h2>
    <button v-on:mouseover="hello('im hello')">Call Hello Function</button>
  </div>
  
</template>

<script>
export default {
    name:'aastha_demo',
    props:{
      data: String,
      msg: String
    },methods:{
      hello(data)
      {
        // console.log('hello console called')
        alert(data)
      }
    }

};
</script>

# data function, conditional , hide, show ,button 
<template>
  <div>
    <h1 v-if="show" > Conditional Rendering in vue.js </h1>
    <!-- <h1 v-else > Conditional Rendering else block </h1> -->
    <button v-on:click="display" >Toggle Element</button>
  </div>
  
</template>

<script>
export default {
    name:'aastha_demo',
    props:{
      data: String,
      msg: String
    },data()
    {
      return {show:true}
    },
    methods:{
      display()
      {
        this.show=!this.show

      }
      
    }
    }

</script>

# for loop code : Home.vue
<template>
  <div>
    <h1>For Loop in vue.js</h1>
    <table border="1px">
      <tr>
        <td>Id</td>
        <td>Name</td>
        <td>Email</td>
      </tr>

      <tr v-for="user in users" :key="user.id">
        <td>{{ user.id }}</td>
        <td>{{ user.name }}</td>
        <td>{{ user.email }}</td>
      </tr>
    </table>
  </div>
  
</template>

<script>
export default {
    name:'aastha_demo',
    props:{
      data: String,
      msg: String
    },data()
    {
      return {
        users:[
          {id:1,name:'peter',email:'peter@test.com'},
          {id:2,name:'Brace',email:'Brace@test.com'},
          {id:3,name:'Jeo',email:'Jeo@test.com'},
          {id:4,name:'Metric',email:'metric@test.com'},
        ]
      }
    }
    }

</script>


