<script>
    import { postData } from './postData.js';
	import Post from "./Post.svelte";
    import Search from "./Search.svelte";
    import NoResults from "./NoResults.svelte";

    let filteredPosts = [];
    let searchTerm = "";
    
    const searchPosts = () => {
        return filteredPosts = postData.filter(post => {
            let postTitle = post.title.toLowerCase();
            return postTitle.includes(searchTerm.toLowerCase());
        })
    }
</script>

<section id="query">
    <Search bind:searchTerm on:input={searchPosts} />
</section>
<main>
    {#if searchTerm && filteredPosts.length === 0}
    <NoResults />
    {:else if filteredPosts.length > 0}
        {#each filteredPosts as {image, title, date}}
            <Post   {image}
                    {title}
                    {date} />
        {/each}
    {:else}
        {#each postData as {image, title, date}}
            <Post   {image}
                    {title}
                    {date} />
        {/each}
    {/if}
</main>

<style>
	section {
		width: 100%;
		display: flex;
		justify-content: center;
	}
    main {
        width: 100%;
		margin: 10px;
		display: flexbox;
		flex-direction: column;
		flex-wrap: wrap;
		justify-content: center;
        background: url('https://www.runescape.com/img/rsp777/bg2.jpg') repeat-y center top;
        background-color: black;
    }
</style>
