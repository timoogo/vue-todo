<template>
  <ul>
    <li>
      <a href="#">content</a>
      <a class="mydelete"  href="#">
        <i class="fas fa-trash"></i>
      </a>
    </li>
    <li>
      <a href="#">content</a>
      <a class="mydelete"  href="#">
        <i class="fas fa-trash"></i>
      </a>
    </li>

  </ul>
</template>

<script>
export default {
name: "ToDoList"
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
</style>