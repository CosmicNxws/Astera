<script>
    const games = [

    {
            title: "Singularity",
            description: "The universe is your all-you-can-eat buffet! Guide your black hole to consume planets while avoiding nasty anti-stars and Those pesky humans in this gravity-powered arcade style game.",
            release: "82% Finished",
            image: "/fileimages/singularity.png"
        },

        {
            title: "Outpost Erebus",
            description: "Manage a remote mining station in the Kuiper Belt. Collect resources, expand your outpost, and survive while growing your profits.",
            release: "Early Development",
            image: "/fileimages/Erebus.png"
        },
        
        {
            title: "Astera Blast",
            description: "The best Shoot'em up asteroid game",
            release: "Early Planning",
            image: "/fileimages/asterablast.png"
        },
        
        {
            title: "MARIS",
            description: "As MARIS-OS, an AI aboard Ares Station, you uncover a conspiricy. Manage the station, make choices, and decide who—or what—you'll become.",
            release: "Early Planning",
            image: "/fileimages/no.png"
        }
    ];
</script>

<svelte:head>
    <title>Astera Interactive</title>
    <meta name="description" content="Creating super cool Space games " />
</svelte:head>

<div class="page-container">
    <section class="hero">
        <div class="hero-content">
            <h2>PUSHING THE FRONTIERS OF GAMING</h2>
            <p class="subtitle">Crafting immersive space adventures that transport players to the farthest reaches of the cosmos</p>
            <div class="cta-buttons">
                <a href="#games" class="cta-primary">EXPLORE GAMES</a>
                <a href="/about" class="cta-secondary">OUR MISSION</a>
            </div>
        </div>
        <div class="stars"></div>
        <div class="twinkling"></div>
    </section>

    <section id="games" class="games-section">
        <div class="section-header">
            <h3>GAMES IN EARLY DEVELOPMENT</h3>
            <div class="divider"></div>
        </div>

        <div class="games-grid">
            {#each games as game}
                <div class="game-card">
                    <div class="game-image" style={`background-image: url('${game.image}')`}>
                        <div class="release-badge">{game.release}</div>
                    </div>
                    <div class="game-info">
                        <h4>{game.title}</h4>
                        <p>{game.description}</p>
                        <a href={`/games/${game.title.toLowerCase().replace(/\s+/g, '-')}`} class="learn-more">LEARN MORE →</a>
                    </div>
                </div>
            {/each}
        </div>
    </section>


    <section id="games" class="games-section">
        <div class="section-header">
            <h3>POTENTAL GAMES - WIP</h3>
            <div class="divider"></div>
        </div>
    </section>

    <section class="about-section">
        <div class="about-content">
            <div class="about-text">
                <h3>ABOUT ASTERA INTERACTIVE</h3>
                <div class="divider"></div>
                <p>Founded in April 2025, Astera Interactive is a small indie game studio trying to make awesome space games. Our staff comprises people from the Space Community, and our goal is to combine our passions for space, game development, and humanity's future into one cohesive package!</p>
                <p>///</p>
                <a href="/about" class="cta-secondary">OUR STORY</a>
            </div>
            <div class="about-image">
                <div class="glow-effect"></div>
            </div>
        </div>
    </section>
</div>

<style>
    @import url('https://fonts.googleapis.com/css2?family=Orbitron:wght@400;700&family=Rajdhani:wght@300;500;700&display=swap');

    :global(body) {
        margin: 0;
        padding: 0;
        background-color: #0a0e17;
        color: #e0e0e0;
        font-family: 'Rajdhani', sans-serif;
        overflow-x: hidden;
    }

  

    /* Hero Section */
    .hero {
        height: 50vh;
        min-height: 600px;
        position: relative;
        display: flex;
        align-items: center;
        justify-content: center;
        overflow: hidden;
        background: radial-gradient(ellipse at bottom, #1B2735 0%, #090A0F 100%);
    }

    .hero-content {
        text-align: center;
        z-index: 10;
        padding: 0 2rem;
        max-width: 800px;
    }

    h2 {
        font-family: 'Orbitron', sans-serif;
        font-size: 3.5rem;
        margin-bottom: 1.5rem;
        color: #fff;
        text-shadow: 0 0 20px rgba(65, 156, 255, 0.7);
        letter-spacing: 3px;
        line-height: 1.2;
    }

    .subtitle {
        font-size: 1.5rem;
        margin-bottom: 3rem;
        color: #a0a8c0;
        font-weight: 300;
    }

    .cta-buttons {
        display: flex;
        gap: 1.5rem;
        justify-content: center;
    }

    .cta-primary, .cta-secondary {
        padding: 1rem 2rem;
        border-radius: 4px;
        font-family: 'Orbitron', sans-serif;
        font-weight: 700;
        text-decoration: none;
        text-transform: uppercase;
        letter-spacing: 1px;
        transition: all 0.3s ease;
    }

    .cta-primary {
        background: linear-gradient(135deg, #41a0ff 0%, #2d6bff 100%);
        color: #fff;
        box-shadow: 0 0 20px rgba(65, 156, 255, 0.5);
    }

    .cta-primary:hover {
        transform: translateY(-3px);
        box-shadow: 0 0 30px rgba(65, 156, 255, 0.8);
    }

    .cta-secondary {
        border: 2px solid #41a0ff;
        color: #41a0ff;
    }

    .cta-secondary:hover {
        background: rgba(65, 156, 255, 0.1);
        transform: translateY(-3px);
    }

    /* Stars Animation */
    @keyframes move-twink-back {
        from {background-position:0 0;}
        to {background-position:-10000px 5000px;}
    }

    .stars, .twinkling {
        position: absolute;
        top: 0;
        left: 0;
        right: 0;
        bottom: 0;
        width: 100%;
        height: 100%;
        display: block;
    }

    .stars {
        background:#000 url('/stars.png') repeat top center;
        z-index: 0;
    }

    .twinkling {
        background:transparent url('/twinkling.png') repeat top center;
        z-index: 1;
        animation:move-twink-back 200s linear infinite;
    }

    /* Games Section */
    .games-section {
        padding: 6rem 2rem;
        max-width: 1200px;
        margin: 0 auto;
    }

    .section-header {
        text-align: center;
        margin-bottom: 4rem;
    }

    h3 {
        font-family: 'Orbitron', sans-serif;
        font-size: 2.5rem;
        color: #fff;
        margin-bottom: 1.5rem;
        letter-spacing: 2px;
    }

    .divider {
        height: 3px;
        width: 100px;
        background: linear-gradient(90deg, #41a0ff 0%, transparent 100%);
        margin: 0 auto 2rem;
    }

    .games-grid {
        display: grid;
        grid-template-columns: repeat(auto-fit, minmax(350px, 1fr));
        gap: 2rem;
    }

    .game-card {
        background: rgba(26, 31, 58, 0.6);
        border-radius: 8px;
        overflow: hidden;
        transition: transform 0.3s ease, box-shadow 0.3s ease;
        border: 1px solid rgba(65, 156, 255, 0.2);
    }

    .game-card:hover {
        transform: translateY(-10px);
        box-shadow: 0 10px 30px rgba(65, 156, 255, 0.2);
    }

    .game-image {
        height: 200px;
        background-size: cover;
        background-position: center;
        position: relative;
    }

    .release-badge {
        position: absolute;
        top: 1rem;
        right: 1rem;
        background: rgba(0, 0, 0, 0.7);
        padding: 0.3rem 0.8rem;
        border-radius: 20px;
        font-size: 0.8rem;
        color: #41a0ff;
        font-weight: 700;
    }

    .game-info {
        padding: 1.5rem;
    }

    h4 {
        font-family: 'Orbitron', sans-serif;
        font-size: 1.5rem;
        margin: 0 0 1rem;
        color: #fff;
    }

    .game-info p {
        color: #a0a8c0;
        margin-bottom: 1.5rem;
        line-height: 1.6;
    }

    .learn-more {
        color: #41a0ff;
        text-decoration: none;
        font-weight: 700;
        display: inline-flex;
        align-items: center;
        gap: 0.5rem;
        transition: all 0.3s ease;
    }

    .learn-more:hover {
        color: #fff;
        text-shadow: 0 0 10px rgba(65, 156, 255, 0.7);
    }

    /* About Section */
    .about-section {
        padding: 6rem 2rem;
        background: linear-gradient(180deg, rgba(10, 14, 23, 0) 0%, rgba(26, 31, 58, 0.7) 100%);
    }

    .about-content {
        max-width: 1200px;
        margin: 0 auto;
        display: grid;
        grid-template-columns: 1fr 1fr;
        gap: 4rem;
        align-items: center;
    }

    .about-text {
        padding-right: 2rem;
    }

    .about-text h3 {
        text-align: left;
    }

    .about-text .divider {
        margin: 0 0 2rem;
    }

    .about-text p {
        margin-bottom: 1.5rem;
        line-height: 1.7;
        color: #a0a8c0;
    }

    .about-image {
        position: relative;
        height: 400px;
        background: url('/space-station.jpg') center/cover no-repeat;
        border-radius: 8px;
        overflow: hidden;
        border: 1px solid rgba(65, 156, 255, 0.3);
    }

    .glow-effect {
        position: absolute;
        top: 0;
        left: 0;
        width: 100%;
        height: 100%;
        background: radial-gradient(circle at center, rgba(65, 156, 255, 0.2) 0%, transparent 70%);
        animation: pulse 4s infinite alternate;
    }

    @keyframes pulse {
        0% { opacity: 0.3; }
        100% { opacity: 0.7; }
    }

    /* Responsive */
    @media (max-width: 768px) {
        h2 {
            font-size: 2.5rem;
        }

        .subtitle {
            font-size: 1.2rem;
        }

        .cta-buttons {
            flex-direction: column;
            gap: 1rem;
        }

        .about-content {
            grid-template-columns: 1fr;
        }

        .about-text {
            padding-right: 0;
        }

        .about-image {
            height: 300px;
        }
    }
</style>