<template>
  <div className="me__kind">
    <h1>AnGyonam은 이런 사람</h1>
    <ol className="kind__ol">
      <li><span>식지 않는 열정</span></li>
      <li><span>조용하게 빠른 적응력</span></li>
      <li><span>뭐든 배우고자 하는 자세</span></li>
    </ol>
  </div>
</template>

<script></script>

<style lang="scss">
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
