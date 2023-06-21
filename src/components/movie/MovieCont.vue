<template>
  <div className="movie__cont container">
    <ul>
      <li v-for="(movie, index) in movies" :key="index">
        <a :href="`https://www.themoviedb.org/movie/${movie.id}`">
          <img :src="`https://image.tmdb.org/t/p/w500/${movie.poster_path}`" />
          <em>
            <p className="title">{{ movie.title }}</p>
            <span className="star">{{ movie.vote_average }}</span>
          </em>
        </a>
      </li>
    </ul>
  </div>
</template>

<script>
export default {
  props: {
    movies: {
      type: Array,
      required: true,
    },
  },
};
</script>

<style lang="scss">
@import "../../assets/scss/setting/mixins.scss";
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
</style>
