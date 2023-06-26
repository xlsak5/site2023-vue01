<template>
  <main>
    <IntroCont />
    <IntroOperate />
    <IntroSkill />
  </main>
</template>

<script>
import IntroCont from "@/components/intro/IntroCont.vue";
import IntroOperate from "@/components/intro/IntroOperate.vue";
import IntroSkill from "@/components/intro/IntroSkill.vue";

export default {
  components: {
    IntroCont,
    IntroSkill,
    IntroOperate,
  },
};
</script>
