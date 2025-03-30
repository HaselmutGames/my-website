<script lang="ts">
    let headline = "HaselmutGames.com";
    let question = "Who am I?";
    let bio = "I'm Hammoud, a Software Developer aspiring to become a Game Developer.🧑‍💻🎮"
    let socials = [
        { name: "GitHub", url: "https://github.com/HaselmutGames" },
        { name: "Twitch", url: "https://www.twitch.tv/haselmutgames" },
        { name: "YouTube", url: "https://www.youtube.com/@HaselmutGames" },
        { name: "X", url: "https://x.com/HaselmutGames" },
    ];
</script>

<main class="container">
    <div class="headline">
        <h1>{headline}</h1>
    </div>
    <h1>{question}</h1>
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
    :global(html){
        font-family: 'Courier New', Courier, monospace;
        background-color: black;
        color: white;
        margin: 0;
        padding: 0;
        height: 100%;
    }
    .container{
        text-align: center;
        margin-top: 50px;  
    }
    .headline{
        color: orange;
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