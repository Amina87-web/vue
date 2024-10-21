<script >
export default{
   data(){
 return{
 name:'',
 list:[]
 }
 },
 methods:{
 test(){
 this.list.push(this.name);
 },
 sor(){
this.list.sort();
 },
dell(){
this.list=0;
}
}
}
</script>  
<template>

  <h1>Мои задачи</h1>
<div class="container">
  <div class="header">
    <input type="text" placeholder="Введи задачу" class="in" v-model="name">
  <button class="btn" @click="test();">Добавить</button>
    </div>


<div class="content">
<div class="task" v-for="x in list">
  <input type="radio" name="task1" class="in_r"><p class="text_task">{{ x }}</p>
</div>
</div>

<div class="footer">
  <hr>
  <button @click="dell();">Удалить</button> <button @click="sor();">Сортировать</button>
</div>
</div>


 
</template>

<style scoped>

</style>