<script>
    import {onMount} from "svelte";
    import PopularMovie from "../components/movie/popularMovie.svelte"

    export let popular = [];
    async function loadMovie() {
        let apiKey = "3bcb08313fe3bc8292a3caf1a96ebac2";
        const res = await fetch(`https://api.themoviedb.org/3/movie/popular?api_key=${apiKey}&language=en-US&page=1`);
        const data = await res.json();
        if (res.ok) {
            popular = data.results;
            console.log(popular,555)
        }
    }
    onMount(async () => {
        await loadMovie();
    })
</script>

<div>
    <PopularMovie popular="{popular}"/>
</div>
