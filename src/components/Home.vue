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

