<template>
  <div>
    <div>hello {{person.name}}</div>
    <div>My age is {{person.age}}</div>
    <div v-if="person.isDev">I am a dev</div>
    <div v-else>I am not a dev</div>
    <button @click="increaseMyAgeAndChangeMyName()">Increase my age</button>
  </div>
</template>
<script>
export default{
data(){
  return{
    person :{
      name:'Nicolas ',
      age:43,
      isDev : false
    }
  }
},
methods:{
  increaseMyAgeAndChangeMyName(){
    this.person.name = 'Kevin'
    this.person.age++
  }
}
}
</script>
