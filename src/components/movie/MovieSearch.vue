<template>
  <div>
    <main>S</main>
  </div>
</template>

<style lang="scss">
@import "../../assets/scss/setting/mixins.scss";
// movies__wrap
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
    @include border(50px);
  }
  .movies__item {
    @include flex-between;
    margin-top: 70px;
    position: absolute;

    > div {
      width: 400px;
      margin-right: 20px;

      img {
        width: 100%;

        @include border(20px);
      }
    }
  }
}

// movie__cont {
.movie__cont {
  ul {
    display: flex;
    flex-wrap: wrap;
    justify-content: space-between;
    font-family: "NanumBarunGothic";

    li {
      width: 23%;
      position: relative;
      margin-bottom: 2%;
      margin-right: 1%;

      .title {
        font-size: 20px;
        padding: 3px 0;
        text-align: center;

        &:hover {
          text-decoration: underline;
          text-underline-position: under;
        }
      }

      .star {
        position: absolute;
        right: 20px;
        top: 20px;
        width: 30px;
        height: 30px;
        background-color: #fff;
        text-align: center;
        line-height: 30px;
        border-radius: 50%;
        font-size: 12px;
        font-weight: bold;
      }
    }
  }
}

// movie__search
.movie__search {
  margin-bottom: 50px;
  text-align: center;

  input {
    border: 1px solid #e8ecf2;
    font-size: 16px;
    padding: 10px 20px;
    @include border(50px);
    min-width: 300px;
    margin-right: 10px;
    font-family: "NanumBarunGothic";
  }

  button {
    @include button(#f7100d, #fff);
    @include border(50px);
    font-family: "NanumBarunGothic";
  }
}
</style>
