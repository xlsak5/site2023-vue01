<template>
  <ContTitle title="movies" />
  <MovieSlider />
  <MovieSearch />
  <MovieTag />
  <MovieCont :movies="movies" />
  <!-- :movies="movies" -->
</template>

<script>
import ContTitle from "@/components/layout/ContTitle.vue";
import MovieSlider from "@/components/movie/MovieSlider.vue";
import MovieSearch from "@/components/movie/MovieSearch.vue";
import MovieTag from "@/components/movie/MovieTag.vue";
import MovieCont from "@/components/movie/MovieCont.vue";
import { ref } from "vue";

export default {
  components: {
    ContTitle,
    MovieSlider,
    MovieSearch,
    MovieTag,
    MovieCont,
  },

  // setup(){}은 그냥 문법이래
  setup() {
    const movies = ref([]);
    const serarchs = ref([]);
    const search = ref("marble");

    const TopMovies = async () => {
      await fetch(
        `https://api.themoviedb.org/3/movie/popular?api_key=ec3680ba547ae5f7c2f1143ff31a8746&query=${search.value}`
      )
        .then((response) => response.json())
        .then((result) => {
          movies.value = result.results;
          serarchs.value = result.results;
          console.log(serarchs);
        })
        .then((error) => console.log("error", error));
    };
    TopMovies();

    return {
      movies,
      serarchs,
      TopMovies,
    };
  },
};
</script>

<style lang="scss">
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
    border-radius: 50px;
  }
  .movies__item {
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
    // @include border(50px);
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
      background-color: darken(#e24c4c, 20%);
    }
    font-family: "NanumBarunGothic";
  }
}
</style>
