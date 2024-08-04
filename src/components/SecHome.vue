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
<h4>Technology</h4><br />
<label for="Node">Node</label>
<input type="checkbox" value="Node" v-model="technology" id="Node"/>
<br>
<label for="React">React</label>
<input type="checkbox" value="React" v-model="technology" id="React"/>
<br />
<label for="Js">Js</label>
<input type="checkbox" value="Js" v-model="technology" id="Js"/>

<br/>
<br/>
<h3>Who Am I</h3>
<br />
<label for="student">Student</label>
<input type="radio" value="student" v-model="who" id="student"/>
<br/>
<label for="developer">Developer</label>
<input type="radio" value="developer" v-model="who" id="developer"/>

<h3>Selected Technology: {{technology}}</h3>
<br/>
<br/>
<h3>Selected Who: {{who}}</h3>
<button type="button" v-on:click="getData()">Submit</button>

<br/>
<br/>

<h3 v-if="show">If true show this </h3>

<h3 v-else>If false Show this </h3>

<br/>
<button v-on:click="show=!show">Toggle</button>


</template>

<script>
 export default{
    name: 'SecHome',
    data(){
        return {
        Email : null,
        Password: null,
        technology:[],
        who:null,
        show: false
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