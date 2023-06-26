<template>
  <div className="port__box">
    <ul>
      <li>
        <a href="#">
          <img
            src="../../../src/assets/images/port/webstandard.png"
            alt="만든 사이트1"
          />

          <div className="port__desc">
            <span>웹표준 사이트입니다.</span>
            <p>6개월 동안 배웠던 것들과 만든 것들을 모아 놓은 사이트입니다.</p>
          </div>
        </a>
      </li>
      <li>
        <a href="#">
          <img
            src="../../../src/assets/images/port/webstandard.png"
            alt="만든 사이트1"
          />

          <div className="port__desc">
            <span>신일전자 메인 페이지 클론 코딩입니다.</span>
            <p>HTML, CSS, JAVASCRIPT로 만든 다음 React로 변환을 했습니다.</p>
          </div>
        </a>
      </li>
      <li>
        <a href="#">
          <img
            src="../../../src/assets/images/port/webstandard.png"
            alt="만든 사이트1"
          />

          <div className="port__desc">
            <span>Vue.js로 제작한 사이트 입니다.</span>
            <p>HTML, CSS로 제작한 다음 VUE.JS로 변환을 하였습니다.</p>
          </div>
        </a>
      </li>
      <li>
        <a href="#">
          <img
            src="../../../src/assets/images/port/webstandard.png"
            alt="만든 사이트1"
          />

          <div className="port__desc">
            <span>PHP로 제작한 팀프로젝트 입니다.</span>
            <p>6개월 동안 배웠던 것들과 만든 것들을 모아 놓은 사이트입니다.</p>
          </div>
        </a>
      </li>
      <li>
        <a href="#">
          <img
            src="../../../src/assets/images/port/webstandard.png"
            alt="만든 사이트1"
          />

          <div className="port__desc">
            <span>JAVASCRIPT로 제작한 게임 입니다.</span>
            <p>6개월 동안 배웠던 것들과 만든 것들을 모아 놓은 사이트입니다.</p>
          </div>
        </a>
      </li>
    </ul>
  </div>
</template>

<script></script>

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
          text-align: center;
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

// PortfolioCont
.port__box {
  width: 1280px;
  margin: 0 auto;
  padding-bottom: 5%;

  ul {
    display: flex;
    flex-wrap: wrap;
    justify-content: space-between;

    li {
      width: 48%;
      text-align: center;
      margin-right: 2%;
      margin-bottom: 3%;
      border: 1px solid rgba(0, 0, 0, 0.1);

      a {
        display: inline-block;
        width: 100%;

        &:hover {
          text-decoration: underline;
          text-underline-position: under;
        }

        img {
          width: 100%;
          border-radius: 5px;
          border-bottom: 1px solid rgba(0, 0, 0, 0.1);
        }

        .port__desc {
          text-align: left;
          font-family: "NanumSquareNeo";
          padding-top: 10px;

          span {
            font-size: 23px;
            font-weight: 700;
          }
          p {
            margin-top: 10px;
            font-size: 18px;
          }
        }
      }
    }
  }
}
</style>
