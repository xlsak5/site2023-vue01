<template>
  <section id="introSkill" className="introSkill bg-blue">
    <h3 className="blind">프론트앤드 커리큘럼 과정 소개</h3>
    <div className="intro__inner container">
      <div className="intro__title">
        <span>My Skill</span>
        <h3>나의 스킬</h3>
        <p>
          프론트앤드 개발자로 취업하기 위한<br />
          전문 과정입니다.
        </p>
      </div>
      <div className="intro__desc">
        <div>
          <h4 className="icon-bg1">React.js</h4>
          <p>
            리액트(React)는 페이스북에서 개발된 자바스크립트 라이브러리입니다.
            이는 사용자 인터페이스를 구축하기 위해 사용됩니다.
          </p>
        </div>
        <div>
          <h4 className="icon-bg2">Vue.js</h4>
          <p>
            Vue.js는 사용자 인터페이스를 구축하기 위한 프로그레시브 자바스크립트
            프레임워크입니다.
          </p>
        </div>
        <div>
          <h4 className="icon-bg3">Next.js</h4>
          <p>
            Next.js는 React의 기능을 확장하여 개발자가 웹 애플리케이션을 빠르고
            효율적으로 구축할 수 있도록 도와줍니다.
          </p>
        </div>
        <div>
          <h4 className="icon-bg4">프론트앤드 개발자</h4>
          <p>
            HTML, CSS 및 JavaScript를 사용하여 웹 페이지를 만들고, 사용자의
            상호작용과 시각적인 요소를 구현합니다.
          </p>
        </div>
      </div>
    </div>
  </section>
</template>

<style lang="scss">
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

// IntroCont
.me__box {
  padding: 10% 0;
  h1 {
    text-align: center;
    font-size: 30px;
    margin-right: 250px;
    margin-bottom: 20px;
    color: #0077ff;
    font-family: "NanumSquareNeo";
    font-weight: bold;
  }
  .me__introduce {
    display: flex;
    justify-content: center;
    align-items: center;
    width: 1280px;
    margin: 0 auto;
    padding-bottom: 5%;

    .introduce__box {
      display: flex;
      justify-content: center;

      img {
        width: 200px;
        background-color: #fae29e;
        border-radius: 50%;
      }

      .introduce__desc {
        display: flex;
        flex-direction: column;
        align-items: center;
        justify-content: center;
        margin-left: 30px;
        ul {
          li {
            margin-bottom: 25px;
            p {
              color: #0077ff;
              font-weight: bold;
              font-size: 23px;
              font-family: "NanumSquareNeo";
            }
            span {
              font-size: 18px;
              font-family: "NanumSquareNeo";
            }
          }
        }
      }
    }
  }
}

// introSkill
.introSkill {
  padding: 10%;
  margin-bottom: 10%;
}

// me__kind
.me__kind {
  display: flex;
  flex-direction: column;
  align-items: center;
  width: 1280px;
  margin: 0 auto;
  padding: 10% 0;
  box-sizing: border-box;

  h1 {
    font-size: 24px;
    font-family: "NanumBarunGothic";
    font-weight: 700;
    margin-bottom: 20px;
    box-sizing: border-box;
  }

  ol.kind__ol {
    li {
      span {
        text-align: left;
        font-size: 22px;
        font-family: "NexonLv2Gothic";
        font-weight: 400;
      }
      &:nth-child(1):before {
        content: "1.";
        font-size: 22px;
      }
      &:nth-child(2):before {
        content: "2.";
        font-size: 22px;
      }
      &:nth-child(3):before {
        content: "3.";
        font-size: 22px;
      }
    }
  }
}
</style>
