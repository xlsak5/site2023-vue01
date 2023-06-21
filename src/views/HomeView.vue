<template>
  <main>
    <SliderSection attr="slider_-wrap section gmarket5" />
    <IntroSection attr="intro__wrap section bg-blue suseong" />
    <PortSection attr="port__wrap section center scoreDream bg-blue" />
    <MovieSection attr="movies__wrap section crown" />
    <YoutubeSection attr="youtube__wrap section crown" />
    <UnsplationSection attr="unsplash__wrap section scoreDream bg-blue" />
  </main>
</template>

<script>
import SliderSection from "@/components/section/SliderSection.vue";
import IntroSection from "@/components/section/IntroSection.vue";
import PortSection from "@/components/section/PortSection.vue";
import MovieSection from "@/components/section/MovieSection.vue";
import YoutubeSection from "@/components/section/YoutubeSection.vue";
import UnsplationSection from "@/components/section/UnsplationSection.vue";

export default {
  components: {
    SliderSection,
    IntroSection,
    PortSection,
    MovieSection,
    YoutubeSection,
    UnsplationSection,
  },
};
</script>
