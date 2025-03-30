<script lang="ts">
    import { icons } from '$lib/data/icons';
    import { socials } from '$lib/data/socials';
    let headline = "HaselmutGames.com";
    let question = "Who am I?";
    let bio = "I'm Hammoud, a Software Developer aspiring to become a Game Developer.🧑‍💻🎮"
</script>

<main class="container">
    <!-- Clickable Headline -->
    <div class="headline">
        <a href="/" class="headline-link">{headline}</a>
    </div>
    <!-- Icons-->
     <div class="icon-links">
        {#each icons as icon}
            <a href={icon.url} class="icon">
                {icon.emoji}
            </a>
            <p> {icon.name}</p>
        {/each}
     </div>

    <h1>{question}</h1>
    <p>{bio}</p>

    <!-- Social Links -->
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
        background-color: grey;
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
        font-size: 2em;
    }
    .headline {
        color: orange;
        font-size: 2rem;
    }
    .headline-link {
        text-decoration: none;
        color: orange;
        font-weight: bold;
    }
    .headline-link:hover {
        text-decoration: underline;
    }
    .icon-links {
        margin: 20px 0;
    }
    .icon {
        font-size: 1.5rem;
        margin: 0 10px;
        text-decoration: none;
    }
    .icon:hover {
        opacity: 0.8;
    }
    ul {
        list-style: none;
        padding: 0;
    }
    li {
        display: inline;
        margin: 0 10px;
    }
</style>