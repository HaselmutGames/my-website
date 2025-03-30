<h1>Welcome to SvelteKit</h1>
<p>Visit <a href="https://svelte.dev/docs/kit">svelte.dev/docs/kit</a> to read the documentation</p>

<script>
    let name = "Hammoud";
    let bio = "I'm Hammoud, a Software Developer aspiring to become a Game Developer.🧑‍💻🎮"
    let socials = [
        { name: "GitHub", url: "https://github.com/HaselmutGames" },
        {name: "Twitch", url: "https://www.twitch.tv/haselmutgames"},
        { name: "YouTube", url: "https://www.youtube.com/@HaselmutGames" },
        { name: "X", url: "https://x.com/HaselmutGames" },
    ];
</script>

<main class="container">
    <h1>{name}</h1>
    <p>{bio}</p>

    <ul>
        {#each socials as social}
            <li>
                <a href={social.url} target="_blank">
                    {social.name}
                </a>
            </li>
        {/each}
    </ul>
</main>

<style>
    .container{
        text-align: center;
        margin-top: 50px;
    }
    ul{
        list-style: none;
        padding: 0;
    }
    li{
        display: inline;
        margin: 0 10px;
    }
</style>