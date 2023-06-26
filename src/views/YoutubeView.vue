<template>
  <ContTitle title="youtube" />
  <YoutubeCont />
  <YoutubeSearch />
  <YoutubeSlider />
  <YoutubeTag />
</template>

<script>
import ContTitle from "@/components/layout/ContTitle.vue";
import YoutubeCont from "@/components/youtube/YoutubeCont.vue";
import YoutubeSearch from "@/components/youtube/YoutubeSearch.vue";
import YoutubeSlider from "@/components/youtube/YoutubeSlider.vue";
import YoutubeTag from "@/components/youtube/YoutubeTag.vue";

export default {
  components: {
    ContTitle,
    YoutubeCont,
    YoutubeSearch,
    YoutubeSlider,
    YoutubeTag,
  },
};
</script>
