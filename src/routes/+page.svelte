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
    <!-- Icons with labels (stacked)-->
     <div class="icon-links">
        {#each icons as icon}
            <div class="icon-item">
                <a href={icon.url} class="icon">
                    {icon.emoji}
                </a>
                <a href={icon.url} class="icon-label">
                    {icon.name}
                </a>
            </div>
        {/each}
     </div>
    <h1>{question}</h1>
    <p>{bio}</p>

    <!-- Social Links -->
    <ul class="social-links">
        {#each socials as social}
            <li>
                <a href={social.url} target="_blank" class="social-link">
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
    .headline-link {
        text-decoration: none;
        color: orange;
        font-weight: bold;
    }
    .headline-link:hover {
        text-decoration: underline;
    }

    /* Icon Section*/
    .icon-links {
        display: flex;
        justify-content: center;
        gap: 20px;
        margin: 20px 0;
    }
    .icon-item{
        display: flex;
        flex-direction: column;
        align-items: center;
    }
    .icon, .icon-label {
        text-decoration: none;
        color: white;
        font-size: 1.5rem;
        margin: 5px 0;
    }
    .icon:hover, .icon-label:hover {
        color: orange;
        cursor: pointer;
        opacity: 0.8;
    }

    /* Social Links */
    .social-link {
        text-decoration: none;
        color: white;
        font-size: 1.2rem;
        padding: 0;
    }
    .social-link:hover {
        color: orange;
    }
</style>