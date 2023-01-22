<template>
 <div class="flex min-h-full items-center justify-center py-12 px-4 sm:px-6 lg:px-8">
  <div class="w-full max-w-md space-y-8">
    <div>
      
      <h2 class="mt-6 text-center text-3xl font-bold tracking-tight animate__fadeInDown">Войди что бы прокоментировать!!</h2>
      <p class="mt-2 text-center text-sm animate__fadeInDown">
        или поставить лайки.
        
        <RouterLink to="/" class="font-medium text-indigo-600 hover:text-indigo-500 animate__fadeInDown">вернутся на главную.</RouterLink>
      </p>
      
    </div>
    <form class="mt-8 space-y-6"  @submit.prevent="submitRegistration" method="POST">
      <input type="hidden" name="remember" value="true">
      <div class="-space-y-px rounded-md shadow-sm">
        <div class="pole">
          <label for="email-address" class="sr-only">Почта</label>
          <input id="email-address"  v-model="email" name="email" type="email" autocomplete="email" required class="relative block w-full appearance-none rounded-none rounded-t-md border border-gray-300 px-3 py-2 text-gray-900 placeholder-gray-500 focus:z-10 focus:border-indigo-500 focus:outline-none focus:ring-indigo-500 sm:text-sm" placeholder="Почта">
        </div>
        <div class="pole">
          <label for="password" class="sr-only">Пароль</label>
          <input id="password" v-model="password" name="password" type="password" autocomplete="current-password" required class="relative block w-full appearance-none rounded-none rounded-b-md border border-gray-300 px-3 py-2 text-gray-900 placeholder-gray-500 focus:z-10 focus:border-indigo-500 focus:outline-none focus:ring-indigo-500 sm:text-sm" placeholder="Пароль">
        </div>
      </div>

   

      <div>
        <button type="submit" class="group relative flex w-full justify-center rounded-md border border-transparent bg-indigo-600 py-2 px-4 text-sm font-medium text-white hover:bg-indigo-700 focus:outline-none focus:ring-2 focus:ring-indigo-500 focus:ring-offset-2">
        
         Вход
        </button>
      </div>
    </form>
  </div>
</div>
<RouterView />
</template>

<script >
import { RouterLink, RouterView } from 'vue-router'

export default {
  data() {
    return {
      email: '',
      password: ''
    }
  }
}
</script>