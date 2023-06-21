<template>
  <div className="unsplash__cont container">
    <ul>
      <li v-for="(unsplash, index) in unsplashs" :key="index">
        <a :href="`https://unsplash.com/photos/${unsplash.id}`">
          <img :src="unsplash.urls.regular" />
        </a>
      </li>
    </ul>
  </div>
</template>

<script>
export default {
  props: {
    unsplashs: {
      type: Array,
      required: true,
    },
  },
};
</script>

<style lang="scss">
@import "../../assets/scss/setting/mixins.scss";
// unsplash__wrap
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
    border-radius: 50px;
  }
  .unsplash__item {
    display: flex;
    justify-content: space-between;
    margin-top: 70px;
    position: absolute;

    > div {
      width: 400px;
      margin-right: 20px;

      img {
        width: 100%;

        border-radius: 20px;
      }
    }
  }
}

// unsplash__page
.unsplash__cont {
  ul {
    column-count: 4;
    column-gap: 20px;

    li {
      // width: 25%;
      margin-bottom: 20px;
    }
  }
}

// unsplash__search
.unsplash__search {
  margin-bottom: 50px;
  text-align: center;

  input {
    border: 1px solid #e8ecf2;
    font-size: 16px;
    padding: 10px 20px;
    border-radius: 50px;
    min-width: 300px;
    margin-right: 10px;
    font-family: "NanumBarunGothic";
  }

  button {
    border-radius: 50px;

    display: inline-block;
    padding: 10px 50px;
    background-color: #e24c4c;
    color: #fff;
    border: 0;
    text-decoration: none;
    cursor: pointer;
    transition: background-color 0.3s;

    &:hover {
      background-color: darken(#b81e1e, 20%);
    }
    font-family: "NanumBarunGothic";
  }
}
</style>
