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


