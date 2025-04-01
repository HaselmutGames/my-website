<script lang="ts">
    import { icons } from '$lib/data/icons';
    import { socials } from '$lib/data/socials';
    // About Section
    let headline = "HaselmutGames";
    let question = "Who am I?";
    let bio = "I am Hammoud (he/him), a software developer aspiring to become a game developer🧑‍💻🎮for my HaselmutGames video game studio. At the University I studied computer science for 3 years in Germany and then started an apprenticeship/working for a company."
    let experience_title = "What do I do?";
    let experience = "I am familiar with both Backend- and Frontend-Frameworks Spring Boot and Angular. In addition, I have worked on several Python projects in laser technology and process development as well as in the development of platforms for analytics and data insights."
    let game_dev_title = "Game-Dev";
    let game_dev_section = "I have always been fascinated by video games so I decided to start learning more about the process of making them. I started learning game development trying to gather as much input as possible while streaming the process live hoping to build a cool community to share my journey and passion with.";

    // Projects Section
    
</script>

<main class="container">
    <!-- Clickable Headline -->
    <div class="headline">
        <a href="/" class="headline-link">{headline}</a>
    </div>
    <!-- About Section-->
    <div class="icon-item">
        <a href={icons[0].url} class="icon-label">
            {icons[0].emoji}
            {icons[0].name}
        </a>
    </div>
    <div class="all-about-me">
        <h1 class="div-titles">{question}</h1>
        <p>{bio}</p>
        <h1 class="div-titles">{experience_title}</h1>
        <p>{experience}</p>
        <h1 class="div-titles">{game_dev_title}</h1>
        <p>{game_dev_section}</p>
    </div> 
    <br>

    <!-- Projects Section-->
    <div class="icon-item">
        <a href={icons[1].url} class="icon-label">
            {icons[1].emoji}
            {icons[1].name}
        </a>
    </div>
    <div>

    </div> 
    <br>

    <!-- Social Links -->
    <ul class="social-links">
        {#each socials as social}
            <div>
                <a href={social.url} target="_blank" class="social-link">
                    {social.name}
                </a>
            </div>
        {/each}
    </ul>
</main>

<style>
    :global(html){
        font-family: 'Courier New', Courier, monospace;
        background-color: rgb(85, 50, 30);
        color: white;
        margin: 0;
        padding: 0;
        height: 100%;
    }
    .container{
        text-align: center;
        margin-top: 50px;
        font-weight: bold;
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

    /* Icon Section */
    .icon-item{
        display: inline-flex;
        align-items: center;
        margin: 20px;
    }
    .icon-label {
        text-decoration: none;
        color: white;
        font-size: 1.5rem;
    }
    .icon-label:hover {
        color: orange;
        cursor: pointer;
        opacity: 0.8;
    }

    .div-titles{
        color: rgb(248, 220, 63);
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