<template>
  <HeaderCont />
  <router-view />
  <FooterCont />
</template>

<style lang="scss">
@import "style.scss";
</style>

<script>
// @ is an alias to /src
import HeaderCont from "@/components/layout/HeaderCont.vue";
import FooterCont from "@/components/layout/FooterCont.vue";

// name 떄문에 에러 남.
export default {
  components: {
    HeaderCont,
    FooterCont,
  },
};
</script>
