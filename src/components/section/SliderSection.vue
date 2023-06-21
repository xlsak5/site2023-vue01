<template>
  <section id="sliderSection" :class="attr">
    <div class="slider__inner">
      <h2 class="blind">배너 슬라이드</h2>

      <swiper
        :modules="modules"
        :slides-per-view="1"
        :space-between="50"
        navigation
        :pagination="{ clickable: true }"
        :scrollbar="{ draggable: true }"
        :autoplay="{
          delay: 2500,
          disableOnInteraction: false,
        }"
        @swiper="onSwiper"
        @slideChange="onSlideChange"
      >
        <swiper-slide v-for="(slider, index) in sliders" :key="index">
          <div class="slider__img">
            <div class="slider__img container">
              <div class="slider s1">
                <div class="text">
                  <h3 v-html="slider.title"></h3>
                  <p v-html="slider.desc"></p>
                  <a href="#" class="more button-red">더 알아보기</a>
                </div>
                <div class="img" aria-label="hidden">
                  <img :src="slider.iconImage1" :alt="slider.title" />
                  <img :src="slider.iconImage2" :alt="slider.title" />
                  <img :src="slider.iconImage3" :alt="slider.title" />
                </div>
                <div class="circle" aria-label="hidden">
                  <span class="circle c1"></span>
                  <span class="circle c2"></span>
                  <span class="circle c3"></span>
                  <span class="circle c4"></span>
                  <span class="circle c5"></span>
                </div>
              </div>
            </div>
          </div>
        </swiper-slide>
      </swiper>
      <div class="slider__btn">
        <a href="#" class="left"><span class="ir">이전 이미지</span></a>
        <a href="#" class="right"><span class="ir">다음 이미지</span></a>
      </div>
      <div class="slider__dot">
        <a href="#" class="dot active"><span class="ir">1번 이미지</span></a>
        <a href="#" class="dot"><span class="ir">2번 이미지</span></a>
        <a href="#" class="dot"><span class="ir">3번 이미지</span></a>
      </div>
    </div>
  </section>
</template>

<script>
// import Swiper core and required modules
import { Navigation, Pagination, Scrollbar, A11y } from "swiper";

// Import Swiper Vue.js components
import { Swiper, SwiperSlide } from "swiper/vue";
import "swiper/css";
import "swiper/css/navigation";
import "swiper/css/pagination";
import "swiper/css/scrollbar";

export default {
  components: {
    Swiper,
    SwiperSlide,
  },
  props: {
    attr: String,
  },
  setup() {
    const onSwiper = (swiper) => {
      console.log(swiper);
    };
    const onSlideChange = () => {
      console.log("slide change");
    };
    return {
      onSwiper,
      onSlideChange,
      modules: [Navigation, Pagination, Scrollbar, A11y],
    };
  },
  data: function () {
    return {
      // public에 이미지가 들어가야 함.
      sliders: [
        {
          title: "New<br />Portfolio",
          desc: "재능은! 노력 끝에서 발견된다.<br /> 어떤 일이라도 노력하고 즐기면 그 어떤것도 뭐라뭐라뭐라",
          iconImage1: "./images/slider/slidericon1.png",
          iconImage2: "./images/slider/slidericon2.png",
          iconImage3: "./images/slider/slidericon3.png",
        },
        {
          title: "New<br />Portfolio",
          desc: "재능은! 노력 끝에서 발견된다.<br /> 어떤 일이라도 노력하고 즐기면 그 어떤것도 뭐라뭐라뭐라",
          iconImage1: "./images/slider/slidericon1.png",
          iconImage2: "./images/slider/slidericon2.png",
          iconImage3: "./images/slider/slidericon3.png",
        },
        {
          title: "New<br />Portfolio",
          desc: "재능은! 노력 끝에서 발견된다.<br /> 어떤 일이라도 노력하고 즐기면 그 어떤것도 뭐라뭐라뭐라",
          iconImage1: "./images/slider/slidericon1.png",
          iconImage2: "./images/slider/slidericon2.png",
          iconImage3: "./images/slider/slidericon3.png",
        },
      ],
    };
  },
};
</script>

<style lang="scss">
.swiper {
  overflow: visible;
}
.swiper-pagination {
  bottom: -80px !important;
}
// slider__wrap
.slider__wrap {
  background-color: #ededed;
}
.slider__inner {
  position: relative;

  .slider__img {
    .slider {
      .text {
        h3 {
          font-size: 110px;
          font-weight: 800;
          text-transform: uppercase;
          line-height: 1;
          margin-bottom: 50px;
        }
        p {
          font-size: 24px;
          line-height: 1.3;
          margin-bottom: 50px;
        }
        .more {
          // mixins.scss에서 효과 줌
          font-size: 18px;
        }
      }
      .img {
        position: absolute;
        right: 0;
        top: -120px;
        width: 600px;
        height: 600px;
        background-image: url(@/assets/images/slider/iconBg.png);
        background-size: cover;

        img {
          &:nth-child(1) {
            width: 300px;
            position: absolute;
          }
          &:nth-child(2) {
            width: 300px;
            position: absolute;
            right: 0;
            bottom: 140px;
          }
          &:nth-child(3) {
            width: 300px;
            position: absolute;
            bottom: 0;
            left: 30px;
          }
        }
      }
      .circle {
        span {
          display: block;
          position: absolute;
          left: 50%;
          top: 50%;
          width: 20px;
          height: 20px;
          border-radius: 50%;
        }
        span:nth-child(1) {
          background-color: var(--button_blue);
          left: 50%;
          width: 10px;
          height: 10px;
        }
        span:nth-child(2) {
          background-color: var(--button_red);
          left: -10%;
          top: 20%;
          width: 40px;
          height: 40px;
        }
        span:nth-child(3) {
          background-color: var(--button_green);
          left: 100%;
          top: 10%;
        }
        span:nth-child(4) {
          background-color: var(--button_red);
          left: 17%;
          top: -10%;
          width: 10px;
          height: 10px;
        }
        span:nth-child(5) {
          background-color: var(--button_blue);
          left: 90%;
          top: 80%;
          width: 30px;
          height: 30px;
        }
      }
    }
  }
  .slider__btn {
    display: inline-block;
    position: absolute;
    top: 50%;
    transform: translateY(-50%);
    width: 22px;
    height: 40px;
    transition: opacity 0.3s;

    &:hover {
      opacity: 0.5;
    }
    .left {
      left: 20px;
      background-image: url(@/assets/images/slider/slider_left.png);
    }
    .right {
      right: 20px;
      background-image: url(@/assets/images/slider/slider_right.png);
    }
  }
  .slider__dot {
    position: absolute;
    left: 50%;
    transform: translateX(-50%);

    .slider__dot {
      position: absolute;
      left: 50%;
      bottom: -80px;
      transform: translateX(-50%);
      a {
        display: inline-block;
        width: 16px;
        height: 16px;
        border-radius: 50%;
        margin: 0 5px;
        border: 4px solid #ff3344;
        background-color: #ff3344;
        box-shadow: 0 0 0 3px transparent;
        &.active {
          box-shadow: 0 0 0 3px #ff3344;
          border-width: 4px;
          background-color: #fff;
        }
      }
    }
    a {
      display: inline-block;
      width: 16px;
      height: 16px;
      border-radius: 50%;
      margin: 0 5px;
      border: 4px solid #ff3344;
      background-color: #ff3344;
      box-shadow: 0 0 0 3px transparent;
      &.active {
        box-shadow: 0 0 0 3px #ff3344;
        border-width: 4px;
        background-color: #fff;
      }
    }
  }
}
</style>
