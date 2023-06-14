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

# template , ok properties, math equation 

<template>
  <div>
    <h1>Template in vue.js</h1>
    <!-- its a behave a constant -->
    <h3 v-once> {{ name }}</h3> 
    <h3> {{ name }}</h3>
    <h3> {{ a + b }}</h3>
    <h3> {{ ok?"Yes":"No" }}</h3>
    <button v-on:click="updateText">Click me</button>

  </div>
</template>

<script>
export default {
    name: "template-demo",
    data()
    {
        return{
            name: 'Aastha',
            a:13,
            b:345,
            ok:true,
        }
    },
    methods: {
        updateText()
        {
            this.name="Peter"
            this.ok=!this.ok
        }
        
    }

}
</script>

<style>

</style>

# Home.vue : disable button , rowHtml 
<template>
  <div>
    <p v-html=" rowHtml"></p>
    
    <!-- its a behave a constant -->
    <h3 v-once> {{ name }}</h3> 
    <h3> {{ name }}</h3>
    <h3> {{ a + b }}</h3>
    <h3> {{ ok?"Yes":"No" }}</h3>
    <button v-bind:disabled="disableBtn" v-on:click="updateText">Click me</button>

  </div>
</template>

<script>
export default {
    name: "template-demo",
    data()
    {
        return{
            name: 'Aastha',
            a:13,
            b:345,
            ok:true,
            rowHtml:"<h1>Template in vue.js</h1>",
            disableBtn:true
        }
    },
    methods: {
        updateText()
        {
            this.name="Peter"
            this.ok=!this.ok
        }
        
    }

}
</script>

<style>

</style>

# style-binding 

<template>
    <h1>CSS binding</h1>
    <h2 class="staticClass" :class="adjustStyle">Home Component</h2>
    <button v-on:click="colorfull=!colorfull">Apply Style</button>
    </template>
    
    <script>
    export default {
        name: "Home-bind",
        data() {
            return {
                colorfull: false
            }
        },
        computed: {
            adjustStyle() {
                return {
                    green: this.colorfull,
                    err: true,
                    other: false
                }
            }
        }
    }
    </script>
    
    <style scoped>
    h1 {
        color: orange
    }
    
    .green {
        background-color: green;
        width: 200px;
        padding: 10px;
        color: #fff
    }
    
    .err {
        color: red
    }
    
    .other {
        font-size: 70px
    }
    </style>

#atyle binding with object

<template>
    <div>
      <h1 class="homestyle"> Class and style bindings</h1>
      <h1 v-bind:style="{color:'blue'}"> Style Bindings </h1>
      <h1 v-bind:class="{display:show}"> Class  Bindings with object </h1>
  
    </div>
  </template>
  
  <script>
  export default {
      name: "style-binding",
      data(){
          return {                
              show:false
          }
      }
  
  }; 
  </script >
  
  <style  scoped>
  .homestyle{
      color:orange
  }
  .display{
      background-color: brown;
  }
  
  </style>
