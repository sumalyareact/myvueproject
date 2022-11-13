<template>
 <div>

  <h1>Register</h1>

  <input 
  type="email"
  name="email"
  v-model="email"
  placeholder="email"/> 

  <br>
  <br>
  <br>

  <input 
  type="password"
  name="password"
  v-model="password"
  placeholder="password"/> 

  <br>
  <br> 

  <button @click="register">Register</button>

</div>
</template>

<script>
import Authenticationservice from '@/services/Authenticationservice'
export default {
    data(){
        return{
            email:'',
            password:''
        }

    },
    methods:{
        async register(){
             await Authenticationservice.register({
                email: this.email,
                password: this.password
            })
            

        }
    }
    
}
</script>

<style scoped>

</style>
