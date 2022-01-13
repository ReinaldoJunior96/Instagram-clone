<template>
  <div class="py-4 px-72 border-b-2 bg-white">
    <div class="flex gap-[210px]">
      <div class="flex gap-[480px]">
        <img
          class=""
          src="https://www.instagram.com/static/images/web/mobile_nav_type_logo.png/735145cfe0a4.png"
          alt=""
        />
        <div class="flex items-center gap-3 bg-gray-100 p-1 rounded-md">
            <i class="fas fa-search text-gray-400"></i>
          <input
            class="0 rounded-md bg-gray-100 text-gray-400 focus:text-black focus:outline-0"
            type="text"
            placeholder="Pesquisar"
          />
        </div>
      </div>
      <div class="flex items-center gap-5">
        <i class="text-lg fas fa-home"></i>
        <i class="text-lg fab fa-facebook-messenger"></i>
        <i class="text-lg far fa-plus-square"></i>
        <i class="text-lg far fa-compass"></i>
        <i class="text-lg far fa-heart"></i>
        <img
          class="w-7 rounded-full"
          src="https://www.listagrupos.com/img-400.400.30-e84f85e5852664c2a1aea5f3c65cf887.jpg"
          alt=""
        />
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "Nav",
};
</script>

<style>
</style>