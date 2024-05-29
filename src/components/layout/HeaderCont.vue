<template>
  <header
    id="header"
    className="header__wrap nexon5 bg-blue"
    role="heading"
    aria-level="1"
  >
    <div className="header__inner container">
      <h1 className="header__logo">
        <router-link to="/"> web <em>site11</em> </router-link>
      </h1>
      <nav className="header__nav" role="navigation">
        <ul>
          <li>
            <router-link to="/intro">소개</router-link>
          </li>
          <li>
            <router-link to="/port">포트폴리오</router-link>
          </li>
          <li>
            <router-link to="/youtube">유튜브</router-link>
          </li>
          <li>
            <router-link to="/unsplash">이미지</router-link>
          </li>
          <li>
            <router-link to="/movie">영화</router-link>
          </li>
        </ul>
      </nav>
    </div>
  </header>
</template>

<style lang="scss">
// header__wrap
.header__wrap {
}
.header__inner {
  text-align: center;

  .header__logo {
    width: 100%;
    font-size: 30px;

    a {
      font-size: 30px;
      display: inline-block;
      padding: 5px;
      margin: 5px;
      text-transform: uppercase;
      font-weight: 800;

      em {
        text-transform: lowercase;
        font-weight: 500;
      }
    }
  }
  .header__nav {
    width: 100%;
    ul {
      padding: 0 10%;
      display: flex;
      justify-content: space-between;

      li {
        a {
          display: inline-block;
          padding: 5px 5px 0px 5px;
          margin: 5px 5px 7px 5px;
          position: relative;
          font-family: "NanumBarunGothic";
          font-weight: 400;

          &::before {
            content: "";
            width: calc(100% - 20px);
            height: 2px;
            background-color: var(--color_body);
            position: absolute;
            left: 10px;
            bottom: -8px;
            transform: scaleX(0);
            transition: all 0.3s ease;
          }

          &:hover::before {
            transform: scaleX(1);
          }
        }
      }
    }
  }
}
</style>
