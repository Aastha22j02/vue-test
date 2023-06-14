#App.vue

<template>
  <div id="app">
    <h1>Form with checkbox and radio button in vue.js</h1>
    <img alt="Vue logo" src="./assets/logo.png">
  <!-- <HelloWorld msg="Welcome to Your Vue.js App"/> -->
  <!-- <Home></Home> -->
    <SignUp/>

  </div>
  
</template>

<script>
// import HelloWorld from './components/HelloWorld.vue'
// import Home from './components/Home.vue'
import SignUp from './components/SignUp.vue'

export default {
  name: 'App',
  components: {
    // HelloWorld
    SignUp
    // Home
    
  }
}
</script>

# 

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>

# signUp.vue

<template>
  <div>
        <input type="text" placeholder="enter your name" v-model="signup.username"/> <br><br>
        <input type="password" placeholder="enter your password" v-model="signup.password"/> <br><br>
        <p>Choose Hobbies</p>
        <input type="checkbox" id="circket" value="circket" v-model="signup.hobbies"/>
        <label for="circket"> Circket

        </label>

        <input type="checkbox" id="football" value="football" v-model="signup.hobbies"/>
        <label for="football"> Football

        </label>
        <br><br>
        <p>Select Gender</p>
        <input type="radio" id="male" value="male" v-model="signup.gender"/>
        <label for="male"> Male

        </label>

        <input type="radio" id="female" value="female" v-model="signup.gender"/>
        <label for="female"> Female

        </label> <br> <br>
        <button v-on:click="signupUser">Sign Up</button>
  </div>
</template>

<script>
export default {
    name: 'Sign-up',
    data()
    {
        return{
            signup:{
                username:null,
                password:null,
                hobbies:[],
                gender:null
            }
        }
    },
    methods:{
        signupUser()
        {
            console.warn(this.signup)
        }
    }

}
</script>

<style>

</style>
