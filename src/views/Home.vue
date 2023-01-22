<template>
 <div class="flex min-h-full items-center justify-center py-12 px-4 sm:px-6 lg:px-8">
  <div class="w-full max-w-md space-y-8">
    <div>
      
      <h2 class="animate__animated animate__bounce mt-6 text-center text-3xl font-bold tracking-tight">Войди что бы прокоментировать!!</h2>
      <p class="mt-2 text-center text-sm ">
        или поставить лайки.
        <RouterLink to="/reg" class="animate__animated animate__bounce font-medium text-indigo-600 hover:text-indigo-500">если нет акаунта зарегайся</RouterLink>
      </p>
      <RouterView />
    </div>
    <form class="mt-8 space-y-6" action="#" method="POST">
      <input type="hidden" name="remember" value="true">
      <div class="-space-y-px rounded-md shadow-sm">
        <div class="pole">
          <label for="email-address" class="sr-only">Почта</label>
          <input id="email-address" name="email" type="email" autocomplete="email" required class="relative block w-full appearance-none rounded-none rounded-t-md border border-gray-300 px-3 py-2 text-gray-900 placeholder-gray-500 focus:z-10 focus:border-indigo-500 focus:outline-none focus:ring-indigo-500 sm:text-sm" placeholder="Почта">
        </div>
        <div class="pole">
          <label for="Имя" class="sr-only">Имя</label>
          <input id="name" name="password" type="name" autocomplete="current-password" required class="relative block w-full appearance-none rounded-none rounded-b-md border border-gray-300 px-3 py-2 text-gray-900 placeholder-gray-500 focus:z-10 focus:border-indigo-500 focus:outline-none focus:ring-indigo-500 sm:text-sm" placeholder="Имя">
        </div>
        <div class="pole">
          <label for="password" class="sr-only">Пароль</label>
          <input id="password" name="password" type="password" autocomplete="current-password" required class="relative block w-full appearance-none rounded-none rounded-b-md border border-gray-300 px-3 py-2 text-gray-900 placeholder-gray-500 focus:z-10 focus:border-indigo-500 focus:outline-none focus:ring-indigo-500 sm:text-sm" placeholder="Пароль">
        </div>
      </div>

   

      <div>
        <button type="submit" class="group relative flex w-full justify-center rounded-md border border-transparent bg-indigo-600 py-2 px-4 text-sm font-medium text-white hover:bg-indigo-700 focus:outline-none focus:ring-2 focus:ring-indigo-500 focus:ring-offset-2">
          <span class="absolute inset-y-0 left-0 flex items-center pl-3">
         
          </span>
         Вход
        </button>
      </div>
    </form>
  </div>
</div>
</template>

<style>
.pole{
  margin-top: 2em;
}
</style>
<script>
import { RouterLink, RouterView } from 'vue-router'


</script>