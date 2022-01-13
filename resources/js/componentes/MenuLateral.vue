<template>
  <div class="p-4">
    <div class="flex p-2 mb-5">
      <div class="flex justify-start items-center">
        <img
          class="w-16 h-16 p-[1px] rounded-full border-[1px] border-red-600"
          src="https://images.pexels.com/photos/7444093/pexels-photo-7444093.jpeg?auto=compress&cs=tinysrgb&w=1260&h=750&dpr=1"
          alt=""
        />
        <div class="flex flex-col">
          <span class="ml-2 text-sm">janelusca.maria</span>
          <span class="text-xs text-gray-400 ml-2">Jade Maria Torres</span>
        </div>
      </div>

      <div class="flex flex-1 justify-end items-center">
        <span class="text-blue-500 text-xs">Mudar</span>
      </div>
    </div>
    <div class="flex p-2">
      <div class="flex justify-start items-center">
        <span class="ml-2 text-xs font-bold text-gray-500"
          >Sugestões para você</span
        >
      </div>

      <div class="flex flex-1 justify-end items-center">
        <span class="text-black text-xs font-bold">Ver tudo</span>
      </div>
    </div>
    <div v-for="img in sugestoes" :key="img" class="flex p-2">
      <div class="flex justify-start items-center">
        <img
          class="w-8 h-8 p-[1px] rounded-full border-[1px]"
          :src="img.foto"
          alt=""
        />
        <div class="flex flex-col">
          <span class="ml-2 text-sm">{{ img.nome }}</span>
          <span class="text-xs text-gray-400 ml-2">{{ img.user }}</span>
        </div>
      </div>

      <div class="flex flex-1 justify-end items-center">
        <span class="text-blue-500 text-xs">Seguir</span>
      </div>
    </div>
    <div class="ml-3 mt-3">
      <span class="text-gray-300 text-sm" >2022 INSTAGRAM FROM <a href="https://github.com/ReinaldoJunior96" target="_blank">ReinaldoJunior96</a>
      </span>
    </div>
  </div>
</template>

<script>
import axios from "axios";
export default {
  name: "MenuLateral",

  data() {
    return {
      sugestoes: [
        {
          foto: "https://images.pexels.com/photos/2253275/pexels-photo-2253275.jpeg?auto=compress&cs=tinysrgb&w=1260&h=750&dpr=1",
          nome: "Shadown",
          user: "shadown.psi",
        },
        {
          foto: "https://images.pexels.com/photos/2820134/pexels-photo-2820134.jpeg?auto=compress&cs=tinysrgb&w=1260&h=750&dpr=1",
          nome: "Jake Peralta",
          user: "jake.p",
        },
        {
          foto: "https://images.pexels.com/photos/1870301/pexels-photo-1870301.jpeg?auto=compress&cs=tinysrgb&w=1260&h=750&dpr=1",
          nome: "Jade",
          user: "Novo no Instagram",
        },
        {
          foto: "https://images.pexels.com/photos/1490908/pexels-photo-1490908.jpeg?auto=compress&cs=tinysrgb&w=1260&h=750&dpr=1",
          nome: "Scott",
          user: "stt.cachorrao",
        },
        {
          foto: "https://images.pexels.com/photos/4453069/pexels-photo-4453069.jpeg?auto=compress&cs=tinysrgb&w=1260&h=750&dpr=1",
          nome: "Cornelios",
          user: "Segestões para você",
        },
      ],
    };
  },
};
</script>

<style>
</style>