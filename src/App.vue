<script setup>
import { RouterLink, RouterView } from 'vue-router'
import HelloWorld from './components/Header.vue'


</script>

<template>
  
 <HelloWorld/>

      <nav>
        <RouterLink to="/" class="linki text-xl text-slate-500">Главная страница</RouterLink>
        <RouterLink to="/about" class="linki text-xl text-slate-500">Регистрация</RouterLink>
        <RouterLink to="/chat"  class=" linki text-xl text-slate-500 ">Чат</RouterLink>
        <RouterLink to="/bio"  class=" linki text-xl text-slate-500 ">О бо мне</RouterLink>
      </nav>
  
  <RouterView />
 
  
</template>

<style scoped>
nav{
  align-items: center;
  text-align: center;
  margin-top: 1em;
}
.linki:hover{
  border-bottom: 2px solid rgb(242, 64, 255);
  transition: 0.3s ease-in;
  color: rgb(72, 5, 255);
}
.linki{
  gap: 3em;
  margin-right: 2em;
}
body{
  color: rgb(179, 76, 243);
}
</style>
