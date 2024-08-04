<template>
<h1>This is my Second Home</h1>
<br />
<br/>
<input type="text" placeholder="Your Email" v-model="Email" />
<br />
<br />
<input type="password" placeholder="Your Password"  v-model="Password"/>
<br/>
<br/>
<button type="button" v-on:click="getData()">Submit</button>
</template>

<script>
 export default{
    name: 'SecHome',
    data(){
        return {
        Email : null,
        Password: null,
        }
    },
    methods:{
        getData(){
           console.warn(this.Email,this.Password);
           
        }

    }
}
</script>

<style>
</style>