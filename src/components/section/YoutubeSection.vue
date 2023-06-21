<template>
  <section id="youtubeSection" :class="attr">
    <div class="youtube__inner container">
      <div class="youtube__text">
        <h3>코딩 유튜버 추천</h3>
        <p>
          더 다양한 강의는 유튜브를 통해 제공하고 있습니다.<br />
          구둑과 좋아요! 부탁드립니다.
        </p>
        <a href="#" class="button-red">자세히 보기</a>
      </div>
      <div class="youtube__item">
        <div>
          <img src="../../assets/images/youtube/you1.png" alt="유튜브1" />
        </div>
        <div>
          <img src="../../assets/images/youtube/you2.png" alt="유튜브2" />
        </div>
        <div>
          <img src="../../assets/images/youtube/you3.png" alt="유튜브3" />
        </div>
        <div>
          <img src="../../assets/images/youtube/you4.png" alt="유튜브4" />
        </div>
        <div>
          <img src="../../assets/images/youtube/you5.png" alt="유튜브1" />
        </div>
        <div>
          <img src="../../assets/images/youtube/you6.png" alt="유튜브3" />
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
// youtube__section
.youtube__wrap {
  overflow: hidden;
}
.youtube__inner {
  height: 570px;

  .youtube__text {
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
  }
  .youtube__item {
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

        // @include border(10px);
        border-radius: 10px;
      }
    }
  }
}

// youtube__page
.youtube__page {
}
.youtube__slider {
  display: none;
}
.youtube__search {
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
    background-color: #ff3344;
    color: #fff;
    border: 0;
    text-decoration: none;
    cursor: pointer;
    transition: background-color 0.3s;

    &:hover {
      background-color: darken(#a01b26, 20%);
    }
    border-radius: 50px;
  }
}
.youtube__tag {
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
.youtube__cont {
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
