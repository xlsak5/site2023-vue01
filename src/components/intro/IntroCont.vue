<template>
  <div className="me__box">
    <h1>About Me</h1>
    <div className="me__introduce">
      <div className="introduce__box">
        <img src="../../assets/images/member/Bust/peep-96.png" alt="안교남" />

        <div className="introduce__desc">
          <ul>
            <li>
              <p>FULL NAME</p>
              <span>An Gyo nam</span>
            </li>
            <li>
              <p>E-MAIL</p>
              <span>skadldldl123@gmail.com</span>
            </li>
            <li>
              <p>BLOG</p>
              <span>asdasdasdasdas</span>
            </li>
          </ul>
        </div>
      </div>
    </div>
  </div>
</template>

<script></script>

<style lang="scss">
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
</style>
