<template>
  <section id="portSection" :class="attr">
    <h3>포트폴리오</h3>
    <p>웹디자이너, 웹 퍼블리셔, 프론트앤드 포트폴리오입니다.</p>
    <div class="port__inner container">
      <div class="port__btn">
        <ul>
          <li><a href="#" class="active">21기</a></li>
          <li><a href="#">22기</a></li>
          <li><a href="#">23기</a></li>
          <li><a href="#">24기</a></li>
        </ul>
      </div>
      <div class="port__cont">
        <div class="port" v-for="(text, index) in texts" :key="index">
          <figure class="member__header">
            <img :src="text.img" :alt="text.title" />
          </figure>
          <div class="port__body">
            <span>
              <img :src="text.icon" :alt="text.title" />
            </span>
            <div class="title">
              <h4>{{ text.title }}</h4>
              <p>{{ text.desc }}</p>
            </div>
          </div>
        </div>
        <!-- port1 -->
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
      texts: [
        {
          img: "../../assets/images/Bust/peep-73.png",
          title: "안교남 포트폴리오",
          desc: "프론트앤드 개발자 포트폴리오",
          icon: "../../assets/images/Bust/peep-73.svg",
        },
        {
          img: "./assets/images/Bust/peep-52.png",
          title: "안교남 포트폴리오",
          desc: "프론트앤드 개발자 포트폴리오",
          icon: "./assets/images/Bust/peep-52.svg",
        },
        {
          img: "./assets/images/Bust/peep-43.png",
          title: "안교남 포트폴리오",
          desc: "프론트앤드 개발자 포트폴리오",
          icon: "./assets/images/Bust/peep-43.svg",
        },
        {
          img: "./assets/images/Bust/peep-54.png",
          title: "안교남 포트폴리오",
          desc: "프론트앤드 개발자 포트폴리오",
          icon: "./assets/images/Bust/peep-54.svg",
        },
        {
          img: "./assets/images/Bust/peep-73.png",
          title: "안교남 포트폴리오",
          desc: "프론트앤드 개발자 포트폴리오",
          icon: "./assets/images/Bust/peep-73.svg",
        },
        {
          img: "./assets/images/Bust/peep-56.png",
          title: "안교남 포트폴리오",
          desc: "프론트앤드 개발자 포트폴리오",
          icon: "./assets/images/Bust/peep-56.svg",
        },
      ],
    };
  },
};
</script>

<style lang="scss">
// port
.port__wrap {
}
.port__inner {
  .port__btn {
    > ul {
      display: flex;
      justify-content: center;

      > li {
        margin: 0 0 45px 0;

        > a {
          display: inline-block;
          width: 126px;
          height: 48px;
          line-height: 48px;
          margin-right: 15px;
          border-radius: 15px;
          font-size: 20px;
          background-color: #eaf0ff;
          box-sizing: border-box;
          transition: all 0.3s;
        }
        > a.active {
          background-color: #d9e4ff;
        }
        &:hover a {
          background-color: #d9e4ff;
        }
      }
    }
  }
  .port__cont {
    display: flex;
    justify-content: space-between;
    flex-wrap: wrap;

    .port {
      width: 32.3333%;
      margin-bottom: 50px;

      > figure {
        border: 1px solid #000;
        border-radius: 5px;

        > img {
        }
      }

      .port__body {
        display: flex;
        margin-top: 10px;
        > span {
          > img {
            display: inline-block;
            width: 50px;
            height: 50px;
            background-color: #f1e8d0;
            border-radius: 50%;
          }
        }
        > div {
          text-align: left;
          margin-left: 10px;
          > h4 {
            font-weight: bold;
            font-size: 18px;
          }
          > p {
            color: #979595;
          }
        }
      }
    }
  }
}
</style>
