<template>
  <div class="px-[285px] py-2 z-30">
    <div class="grid grid-cols-12 gap-5 z-30">
      <div class="col-span-8 z-50">
        <div
          @click="scrollToLeftStories"
          class="
            cursor-pointer
            bg-white
            p-2
            rounded-full
            h-8
            w-8
            absolute
            left-[300px]
            top-24
            shadow-lg
            z-50
          "
        >
          <i class="fas fa-chevron-left absolute top-2 left-3"></i>
        </div>
        <div
          @click="scrollToRightStories"
          class="
            cursor-pointer
            bg-white
            p-2
            rounded-full
            h-8
            w-8
            absolute
            right-[750px]
            top-24
            shadow-lg
            z-50
          "
        >
          <i class="fas fa-chevron-right absolute top-2 right-3"></i>
        </div>
        <div
          class="
            bg-white
            p-3
            border-[1px]
            rounded-sm
            flex
            overflow-hidden
            gap-3
            relative
            stories
          "
        >
          <div
            v-for="(img, index) in photos"
            :key="img"
            class="flex-col text-center justify-center relative"
          >
            <img
              class="
                w-12
                h-11
                p-[1px]
                rounded-full
                border-[1px] border-red-600
                mx-auto
              "
              :src="img.message"
              alt=""
            />
            <span class="text-xs">Doguinho.{{ index }}</span>
          </div>
        </div>
        <div class="">
          <Post />
        </div>
      </div>

      <div class="col-span-4 z-50">
        <MenuLateral />
      </div>
    </div>
  </div>
</template>

<script>
import axios from "axios";
import Post from "../componentes/Post.vue";
import MenuLateral from "../componentes/MenuLateral.vue";
export default {
  components: {
    Post,
    MenuLateral,
  },
  data() {
    return {
      photos: [],
    };
  },
  methods: {
    scrollToRightStories: function () {
      document.querySelector(".stories").scrollLeft += 300;
    },
    scrollToLeftStories: function () {
      document.querySelector(".stories").scrollLeft -= 300;
    },
  },
  mounted() {
    self = this;
    for (var i = 0; i < 30; i++) {
      axios
        .get("https://dog.ceo/api/breeds/image/random")
        .then(function (response) {
          self.photos.push(response.data);
        });
    }
  },
};
</script>

<style>
.stories {
  scroll-behavior: smooth;
}
</style>