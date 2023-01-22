<template>
<div class="con">


<div class="container">
<div class="flex flex-col-reverse">
  <div v-for="(tweet, index) in tweetList" :key="index" class="w-full p-4 border-b hover:bg-lighter flex">
    <div class="flex-none mr-4">
      <img src="https://sun9-west.userapi.com/sun9-46/s/v1/ig2/jo79LhqJaOUQ9POznepYfY2Q0kk_6uyp46ZSiVfwPuITKsEY1l8Pt-k6X-8agw-dpk-uNYtWA6zTBQJzg1UO1-kP.jpg?size=1200x1200&quality=95&type=album" class="h-12 w-12 rounded-full flex-none"/>
    </div>
    <div>
      <div class="flex items-center w-full">
        <p class="font-semibold animate__heartBeat">Nikita_Fronter </p>
        <p class="text-sm text-dark ml-2 animate__heartBeat"> @noder </p>
        <i class="fas fa-angle-down text-dark ml-auto"></i>
      </div>
      <p class="py-2">
        {{ tweet.text }}
      </p>
      <div class="icons flex items-center  w-full">
        <div class="flex items-center text-sm text-dark">
          <i class="far fa-comment mr-3"></i>
          <p> 1 </p>
        </div>
        
        <div class="flex items-center text-sm text-dark">
          <i class="fas fa-heart mr-3"></i>
          <p> 2 </p>
        </div>
        
      </div>
    </div>
  </div>
</div>
<div class="flex flex-col-reverse">
  <div v-for="(tweet, index) in tweetList" :key="index" class="w-full p-4 border-b hover:bg-lighter flex">
    <div class="flex-none mr-4">
      <img src="https://sun9-west.userapi.com/sun9-46/s/v1/ig2/jo79LhqJaOUQ9POznepYfY2Q0kk_6uyp46ZSiVfwPuITKsEY1l8Pt-k6X-8agw-dpk-uNYtWA6zTBQJzg1UO1-kP.jpg?size=1200x1200&quality=95&type=album" class="h-12 w-12 rounded-full flex-none"/>
    </div>
    <div>
      <div class="flex items-center w-full">
        <p class="font-semibold animate__heartBeat">Nikita_Fronter </p>
        <p class="text-sm text-dark ml-2 animate__heartBeat"> @noder </p>
        <i class="fas fa-angle-down text-dark ml-auto"></i>
      </div>
      <p class="py-2">
        {{ tweet.text_two }}
      </p>
      <img class="posts_img" src="https://otkritkis.com/wp-content/uploads/2022/02/1464729791156456568.jpg" alt="">
      <div class="flex items-center icons w-full">
        <div class="flex items-center text-sm text-dark">
          <i class="far fa-comment mr-3"></i>
          <p> 1 </p>
        </div>
      
        <div class="flex items-center text-sm text-dark">
          <i class="fas fa-heart mr-3"></i>
          <p> 2 </p>
        </div>
       
      </div>
    </div>
  </div>
</div>
</div>
<div class="container">
  <lis/>
</div>
</div>
    </template>
    <script>
    import lis from '../components/ListUsers.vue'
    export default{
      components:{
         lis
      },
        data() {
            
        return {
            tweetList: [
        { text: 'Скоро сделаю чат для зарегистрированых!!!',
           text_two:'HAHAHA Норм мем'}
      ],
       tweet: {text: ''}     
        }
    },
    methods: {
    addTweet () {
      let temp = {
        text: this.tweet.text
      };
      this.tweetList.push(temp)
	this.tweet = {
        text : ""
      }
    }
  }
    
    
    
    }
</script>
<style>
.con{
  display: flex;
  margin-top: 6em;
}
.posts_img{
  height: 50%;
}
.icons{
  gap: 2em;
}
i:hover{
  color: rgb(255, 100, 100);
  transition: 0.6s ease-in-out;
}
</style>