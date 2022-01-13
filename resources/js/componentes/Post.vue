<template>
  <div class="">
    <div v-for="post in posts" :key="post" class="border-[1px] mt-5 bg-white">
      <div class="flex p-2">
        <div class="flex justify-start items-center">
          <img
            class="w-8 h-8 p-[1px] rounded-full border-[1px] border-red-600"
            :src="post.foto"
            alt=""
          />
          <span class="ml-2 text-sm">{{ post.user }}</span>
        </div>

        <div class="flex flex-1 justify-end items-center">
          <i class="fas fa-ellipsis-h"></i>
        </div>
      </div>
      <div class="flex flex-col">
        <img :src="post.foto" alt="" />
      </div>
      <div class="flex px-2 pt-3">
        <div class="flex gap-3 justify-start items-center">
          <i class="text-lg far fa-heart"></i>
          <i class="text-lg far fa-comment"></i>
          <i class="text-lg far fa-paper-plane"></i>
        </div>

        <div class="flex flex-1 justify-end items-center">
          <i class="text-lg far fa-bookmark"></i>
        </div>
      </div>
      <div class="pl-2 pt-3">
        <span class="text-sm">{{ post.likes }} curtidas</span>
      </div>
      <div class="pl-2 pt-1">
        <span class="text-sm"
          ><strong>{{post.user}}</strong> {{post.legenda}}</span
        >
      </div>
      <div class="pl-2 pt-1">
        <span class="font-normal text-gray-400 text-sm"
          >Ver todos os {{ post.comentarios }} comentários</span
        >
      </div>
      <div class="pl-2 pt-1">
        <span class="font-normal text-gray-400 text-xs">HÁ {{ post.horas }} HORAS</span>
      </div>
      <div class="flex p-4 border-t-[1px] mt-3">
        <div class="flex items-center gap-3 justify-start">
          <i class="far fa-grin-beam"></i>
          <span class="text-sm text-gray-400">Adicione um comentário</span>
        </div>
        <div class="flex flex-1 justify-end">
          <span class="text-sm text-blue-400">publicar</span>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "Post",

  data(){
    return{
      posts:[
        {
          foto:'https://images.pexels.com/photos/1108099/pexels-photo-1108099.jpeg?auto=compress&cs=tinysrgb&h=750&w=1260',
          user:'labrador.show',
          likes: 453,
          legenda:'Eles crescem tão rapido',
          comentarios: 32,
          horas:4
        },
        {
          foto:'https://images.pexels.com/photos/850602/pexels-photo-850602.jpeg?auto=compress&cs=tinysrgb&h=750&w=1260',
          user:'Joe.png',
          likes:23,
          legenda:'Irmãos <3',
          comentarios:56,
          horas:2
        },
        {
          foto:'https://images.pexels.com/photos/1633522/pexels-photo-1633522.jpeg?auto=compress&cs=tinysrgb&h=750&w=1260',
          user:'k9.police',
          likes:877,
          legenda:'O dia com ela',
          comentarios:65,
          horas:6
        },
      ]
    }
  }
};
</script>

<style>
</style>