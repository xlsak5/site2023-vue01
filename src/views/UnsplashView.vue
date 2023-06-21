<template>
  <UnsplashSlider />
  <UnsplashSearch />
  <UnsplashTag />
  <UnsplashCont :unsplashs="unsplashs" />
</template>

<script>
import UnsplashCont from "@/components/unsplash/UnsplashCont.vue";
import UnsplashSearch from "@/components/unsplash/UnsplashSearch.vue";
import UnsplashSlider from "@/components/unsplash/UnsplashSlider.vue";
import UnsplashTag from "@/components/unsplash/UnsplashTag.vue";
import { ref } from "vue";

export default {
  components: {
    UnsplashCont,
    UnsplashSearch,
    UnsplashSlider,
    UnsplashTag,
  },

  setup() {
    const unsplashs = ref([]);

    // async + await : 동기식
    const search = async () => {
      await fetch(
        `https://api.unsplash.com/search/photos?client_id=r6e6_4ZwiAV0Dc0WvGopVnh2YGoPLi5X-C52UOikVNc&query=1&per_page=30`
      )
        .then((response) => response.json())
        .then((result) => {
          unsplashs.value = result.results;
          console.log("result: ", result);
          console.log("result value: ", result.results);
        })
        .catch((error) => error);
    };
    search();

    return {
      unsplashs,
      search,
    };
  },
};
</script>
