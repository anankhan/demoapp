<template>
  <form @submit.prevent="validatePasswordLength">
   <label>Email :</label>
   <input type="email" required v-model="email" >
    <label>Password :</label>
   <input type="password" required v-model="password" >
   <div class="error" v-if="passwordError" >{{passwordError}}</div>

   <div class="submit" >
       <button >Signup</button>
   </div>
  </form>

  <p>Email :  {{email}}</p>
  <p>Passowrd :  {{password}}</p>
</template>

<script>
export default {
 data()
 {

    return {
        email: '',
        password: '',
        passwordError: ''
         }
     
 },
 methods: {
 
 handleSubmit()
 {
    
     console.log("form submitted");
 },
 validatePasswordLength()
 {
     this.passwordError = this.password.length > 6 ? "" : 'Passowrd Must be atleast 8 chars';
     console.log("Password validated");
 }
 }
}
</script>

<style>

form{
    max-width: 420px;
    margin: 30px auto;
    background: white;
    text-align: left;
    padding: 40px;
    border-radius: 10px;
    }
label{
    color: #aaa;
    display: inline-block;
    font-size: 0.6em;
    font-weight: bold;
    }
    input, select{
        display:block;
        color:#555;
        padding:10px 6px;
        width : 100%;
        box-sizing: border-box;
        border-bottom: 1px solid #ddd;
        }

    button{
        background: blue;
        border: 0;
        padding : 10px 20px;
        margin-top:20px;
        color: white;
        border-radius: 20px;

    }      

    .submit
    {
        text-align : center;
        
    }
    .error
    {
        color: red
    }

</style>