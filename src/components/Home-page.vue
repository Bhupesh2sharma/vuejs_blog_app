<template>
  <h1>Home Page</h1>
  <h1>{{email}}</h1>
<h1> name: : {{getName("Bhupesh")}}</h1>
<h1> Email : {{getEmail().age}}  </h1>
<button v-on:click="getInc()">click me</button>
<button v-on:dblclick="getData('this is double click happening')">click here</button>
<h1>{{count}}</h1>
<input type="text" v-model = "Inc"/>
<h1>{{Inc}}</h1>
</template>

<script>
export default {
  name: 'HomePage',
  data(){
    return{
      Inc : 10,
      count : 0,
      email:"Bhupesh@23",
    }
  },
  methods:{

    getInc(){
       this.count = this.count+1
    },
   
    getName(name){
      return name
    },

    getEmail(){
      return {
        
       email: this.email,
       age : '21'
    }
    },
    getData(data){
    alert(data)

    }
  }
}
</script>

<style scoped>

h1{
  color : green;
}

</style>