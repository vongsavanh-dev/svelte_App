<script>
    import '@fontsource/roboto'
    export let movie;
</script>

<div class="card-movie">
    <div class="image-card-movie">
        <img src="{'https://image.tmdb.org/t/p/w500/' + movie.poster_path}" alt="{movie.title}">
    </div>
    <div class="description-movie">
        <h3>{movie.title}</h3>
        <p>{movie.overview}</p>
        <br>
        <p class="rale-date"><span>Rales date</span>: {movie.release_date}</p>
        <p class="average"><span>Vote Average</span> : {movie.vote_average}</p>
    </div>
</div>

<style lang="scss">
  .card-movie{
    cursor: pointer;
  }
  .description-movie{
    font-family: 'Roboto',sans-serif;
    h3{
      font-size: 1.2rem;
      letter-spacing: 0.5px;
      margin: 10px 0;
      font-weight: 500;
    }
    p{
      margin: 2px;
      text-align: start;
      font-weight: 400;
    }
    .rale-date{
      color: #1635ff;
      span{
        color: black;
        font-weight: 400;
      }
    }
    .average{
      color: #ffa400;
      span{
        color: black;
        font-weight: 400;
      }
    }
  }
  img {
    width: 100%;
    border-radius: 12px;
  }
</style>