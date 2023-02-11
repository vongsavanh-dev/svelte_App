<script>
    import CardMovie from "./cardMovie.svelte";
    export let popular;
</script>


<div class="popular-movie">
    {#each popular as movie}
        <CardMovie {movie}/>
    {/each}
</div>

<style lang="scss">
    .popular-movie{
      display: grid;
      grid-template-columns: repeat(auto-fit,minmax(250px,1fr));
      grid-column-gap: 1rem;
      grid-row-gap: 2rem;
      padding: 40px;
    }
</style>
