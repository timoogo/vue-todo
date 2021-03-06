<template>
  <article class="ToDoCard">
    <header>
      <h2>{{date}}</h2>
<!-- <h2>Mardi 72 février</h2> -->
      <h2 class="highlight">{{title}}</h2>
     <!-- <h2>5 tâches</h2> -->
      <h2>{{tasks.length}} tâche(s) </h2>
    </header>
    <section class="main">
      <!--newTodo-->
      <NewTodo @newTask="addTask"/>
      <!-- end  -->
      <ToDoList/>
    </section>
  </article>

</template>
<script>
import NewTodo from '@/components/NewTodo';
import ToDoList from '@/components/ToDoList';
export default {
  data() {
   return {
      title: "VueJs Tutorial ToDo List",
      tasks: [],
    }

  },
  methods: {
     addTask:function(payload){
       this.tasks.push(payload);
        console.log(this.tasks);
     }
  },
  computed: {
    date: function(){
      let currentDate = new Date()
      return `${currentDate.getDay()} / ${currentDate.getMonth()+1} / ${currentDate.getFullYear()}`
    }
  },

  components:{
    ToDoList,
    NewTodo,
  },
  name: "ToDoCard",

}
</script>

<style>
  article{
    display: flex;
    flex-direction: column;
    background-color: #fff;
    width: 40vw;
    height: 40vh;
    border-radius: 20px ;
    padding: 15px;
  }
  article header{
    display: flex;
    flex-direction: row;
    justify-content: space-between;
  }
  .highlight{
    color: #42b983;
  }
</style>
