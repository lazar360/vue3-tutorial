<template>
  <div>
    <div>Add a todo :</div>
    <input type="text" v-model="value">
    <button @click="addToTodo">Add to todolist</button>
        <div>My todolist :</div>
        <ul>
          <li v-for="(item, itemIndex) in toDolist" v-bind:key="itemIndex">
             {{item}}
          </li>
        </ul>


  </div>
</template>
<script>
export default{
data(){
  return{
    toDolist : ['Go to the haircutter', 'buy some coffee', 'Go to work'],
     value: undefined
    }
  },
  methods : { 
      addToTodo() {
      this.toDolist.push(this.value)
      this.value=undefined
    }
  }
}
</script>
