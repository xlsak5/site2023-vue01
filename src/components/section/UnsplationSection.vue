<template>
  <section id="unsplashSection" :class="attr">
    <div class="unsplash__inner container">
      <div class="unsplash__text">
        <h3>코딩 이미지 추천</h3>
        <p>
          이미지 처리는 디지털 이미지를 분석하고 수정하는 프로세스입니다.<br />
          이를 위해 주로 프로그래밍 언어와 특정 라이브러리를 사용합니다.
        </p>
        <a href="#" class="button-blue">자세히 보기</a>
      </div>
      <div class="unsplash__item">
        <div>
          <img
            src="../../assets/images/unsplash/unsplash1.png"
            alt="코딩 이미지1"
          />
        </div>
        <div>
          <img
            src="../../assets/images/unsplash/unsplash2.png"
            alt="코딩 이미지2"
          />
        </div>
        <div>
          <img
            src="../../assets/images/unsplash/unsplash3.png"
            alt="코딩 이미지3"
          />
        </div>
        <div>
          <img
            src="../../assets/images/unsplash/unsplash4.png"
            alt="코딩 이미지4"
          />
        </div>
        <div>
          <img
            src="../../assets/images/unsplash/unsplash5.png"
            alt="코딩 이미지5"
          />
        </div>
        <div>
          <img
            src="../../assets/images/unsplash/unsplash6.png"
            alt="코딩 이미지6"
          />
        </div>
      </div>
    </div>
  </section>
</template>

<script>
export default {
  props: {
    attr: String,
  },
};
</script>

<style lang="scss">
// unsplash__section
.unsplash__wrap {
  overflow: hidden;
}
.unsplash__inner {
  height: 570px;

  h3 {
    font-size: 50px;
    margin-bottom: 40px;
  }
  p {
    font-size: 20px;
    font-weight: 300;
    margin-bottom: 60px;
  }
  a {
    // @include border(50px);
    border-radius: 50px;
  }
  .unsplash__item {
    // @include flex-between;
    display: flex;
    justify-content: space-between;
    margin-top: 70px;
    position: absolute;

    > div {
      width: 400px;
      margin-right: 20px;

      img {
        width: 100%;

        // @include border(20px);
        border-radius: 20px;
      }
    }
  }
}

// unsplash__page
.unsplash__page {
}
.unsplash__slider {
  display: none;
}
.unsplash__search {
  text-align: center;
  margin-bottom: 50px;

  input {
    // @include border(50px);
    border-radius: 50px;
    border: 1px solid #e8ecf2;
    font-size: 16px;
    padding: 10px 20px;
    min-width: 200px;
    margin-right: 10px;
  }
  button {
    // background-color / color
    // @include button(#f7100d, #fff);
    // @include border(50px);
    display: inline-block;
    padding: 10px 50px;
    background-color: #4857ec;
    color: #fff;
    border: 0;
    text-decoration: none;
    cursor: pointer;
    transition: background-color 0.3s;

    &:hover {
      background-color: darken(#1925a5, 20%);
    }
    border-radius: 50px;
  }
}
.unsplash__tag {
  ul {
    display: flex;
    justify-content: center;
    margin-bottom: 50px;
    margin-top: 50px;

    li {
      margin-right: 25px;
      a {
        border: 1px solid #8a8a8a;
        padding: 10px 20px;
        margin: 0 auto;
        color: #f7100d;
      }
    }
  }
}
.unsplash__cont {
  ul {
    display: flex;
    flex-wrap: wrap;
    justify-content: space-between;
    margin-bottom: 100px;

    li {
      width: 31.3333%;
      margin-bottom: 4%;

      span {
        display: block;
        margin: 4px 0;
      }
    }
  }
}
</style>
