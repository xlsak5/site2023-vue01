<template>
  <section id="introSection" :class="attr">
    <h3 class="blind">프론트앤드 커리큘럼 과정 소개</h3>
    <div class="intro__inner container">
      <div class="intro__title">
        <span>frontend</span>
        <h3 v-html="title"></h3>
        <p v-html="desc"></p>
      </div>
      <div class="intro__desc">
        <div v-for="(text, index) in texts" :key="index">
          <h4 :class="'icon-bg' + (index + 1)">{{ text.title }}</h4>
          <p>
            {{ text.desc }}
          </p>
        </div>
        <!-- <div>
          <h4 class="icon-bg1"></h4>
          <p></p>
        </div> -->
      </div>
    </div>
  </section>
</template>

<script>
export default {
  props: {
    attr: String,
  },
  data: function () {
    return {
      title: "프론트앤드<br />전문과정",
      desc: "프론트앤드 개발자로 취업하기 위한 전문 과정입니다.<br /> 여러분들도 도전해보세요!",
      texts: [
        {
          title: "React.js",
          desc: "리액트(React)는 페이스북에서 개발된 자바스크립트 라이브러리입니다.이는 사용자 인터페이스를 구축하기 위해 사용됩니다.",
        },
        {
          title: "Vue.js",
          desc: "Vue.js는 사용자 인터페이스를 구축하기 위한 프로그레시브 자바스크립트 프레임워크입니다.",
        },
        {
          title: "Next.js",
          desc: "Next.js는 React의 기능을 확장하여 개발자가 웹 애플리케이션을 빠르고 효율적으로 구축할 수 있도록 도와줍니다.",
        },
        {
          title: "프론트앤드 개발자",
          desc: "HTML, CSS 및 JavaScript를 사용하여 웹 페이지를 만들고, 사용자의 상호작용과 시각적인 요소를 구현합니다.",
        },
      ],
    };
  },
};
</script>

<style lang="scss">
@import "../../assets/scss/setting/mixins.scss";
// intro__wrap
.intro__wrap {
}
.intro__inner {
  display: flex;
  justify-content: space-between;
}
.intro__title {
  width: 33%;
  span {
    background-color: #ff3344;
    font-size: 14px;
    padding: 4px 30px 2px;
    color: #fff;
    border-radius: 40px;
    text-transform: uppercase;
    margin-bottom: 10px;
    display: inline-block;
  }
  h3 {
    font-size: 50px;
    font-weight: 700;
    line-height: 1.2;
    margin-bottom: 30px;
  }
  p {
    font-size: 18px;
    line-height: 1.5;
    font-weight: 500;
  }
}
.intro__desc {
  width: 66%;
  display: flex;
  flex-wrap: wrap;
  justify-content: space-between;

  > div {
    width: 48%;
    margin-bottom: 40px;

    h4 {
      font-size: 24px;
      margin-bottom: 15px;
    }
    &:nth-child(3) {
      margin-bottom: 0;
    }
    &:nth-child(4) {
      margin-bottom: 0;
    }
  }
}
</style>
