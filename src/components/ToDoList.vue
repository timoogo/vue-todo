<template>
  <ul>
    <li v-for="task in $parent.tasks"  v-bind:key="task">
    <div class="task">
      <input type="checkbox" name="a">
      <a href="#">{{ task.name }}</a>
    </div>
      <a class="mydelete"  href="#">
        <i class="fas fa-trash"></i>
      </a>
    </li>

  </ul>
</template>

<script>
export default {

name: "ToDoList",
  data() {
    return this

  }
}
</script>

<style scoped>
  ul{
    display: flex;
    flex-direction: column;
  }
  ul li{
    display: flex;
    justify-content: space-between;
    margin: 10px 25px;
    align-items: center;
    padding-left: 5px;
  }
  li:hover{
    background-color :lightgrey;
    color:#fff;


  }
  ul li a.mydelete{
    padding: 12px 20px;
    background-color: red;
    border-radius: 50%;
    height: auto;
    color: #fff !important;
  }
  ul li div.task{
    display: flex;
    flex-direction: row;
    justify-content: space-between;
    width: 30%;
    align-items: center;
  }
  div.task input[type = "checkbox"]{
    border-radius: 50%;
  }
</style>