<template>
  <div>
    <label for="task"></label>
    <input v-model="taskname" id="task" type="text" placeholder="Nouvelle tâches..."/>
    <button @click="sendTask(taskname) ">+</button>
  </div>
</template>
<script>
export default {

  name: "NewTodo",

  methods: {
    sendTask (taskname){
      this.$emit("newTask", { name: taskname} )
    }

  }
}
</script>


<style>
input[type="text"]{
  width: 80%;
  padding: 10px;
  border: 0;
  border-bottom: 2px solid #42b983;
}
input[type="text"]::placeholder{
  text-align: center;
  font-size: 20px;
  color: #b0b0b0;
}
button{
  width: 50px;
  height: 50px;
  border: 0;
  background-color: #42b983;
  border-radius: 50%;
  color: #fff;
  font-size: 20px;
}
</style>