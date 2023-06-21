<template>
  <section id="moviesSection" :class="attr">
    <div class="movies__inner container">
      <div class="movies__text">
        <h3>코딩 영화 추천</h3>
        <p>
          영화는 컴퓨터 과학, 인공 지능, 해킹, 가상 현실, 로봇 공학 등과<br />
          관련된 주제를 다루며, 종종 과학 기술 요소를 역동적이고 시각적으로
          표현합니다.
        </p>
        <a href="#" class="button-green">자세히 보기</a>
      </div>
      <div class="movies__item">
        <div>
          <img src="../../assets/images/movie/movie1.png" alt="영화1" />
        </div>
        <div>
          <img src="../../assets/images/movie/movie2.jpg" alt="영화2" />
        </div>
        <div>
          <img src="../../assets/images/movie/movie3.jpg" alt="영화3" />
        </div>
        <div>
          <img src="../../assets/images/movie/movie4.jpg" alt="영화4" />
        </div>
        <div>
          <img src="../../assets/images/movie/movie5.jpg" alt="영화5" />
        </div>
        <div>
          <img src="../../assets/images/movie/movie6.jpg" alt="영화6" />
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
// movies__section
.movies__wrap {
  overflow: hidden;
}
.movies__inner {
  height: 1000px;

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
  .movies__item {
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

// movie__page
.movie__page {
}
.movie__slider {
  display: none;
}
.movie__search {
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
    background-color: #00c183;
    color: #fff;
    border: 0;
    text-decoration: none;
    cursor: pointer;
    transition: background-color 0.3s;
    border-radius: 50px;

    &:hover {
      background-color: darken(#09684a, 20%);
    }
  }
}
.movie__tag {
  ul {
    display: flex;
    justify-content: center;
    margin-bottom: 50px;
    margin-top: 50px;

    li {
      margin-right: 15px;
      a {
        border: 1px solid #8a8a8a;
        border-radius: 20px;
        padding: 10px 20px;
        margin: 0 auto;
        color: #f7100d;
      }
    }
  }
}
.movie__cont {
  ul {
    display: flex;
    flex-wrap: wrap;
    justify-content: space-between;
    margin-bottom: 100px;

    li {
      width: 19%;
      margin-bottom: 4%;
      margin-right: 1%;

      img {
        width: 100%;
        border-radius: 15px;
      }

      span {
        display: block;
        margin: 4px 0;
      }
    }
  }
}
</style>
