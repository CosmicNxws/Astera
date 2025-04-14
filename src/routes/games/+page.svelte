<script>
    const games = [
        {
            title: "Outpost Erebus",
            description: "Manage a remote mining station in the Kuiper Belt. Collect resources, expand your outpost, and survive while growing your profits.",
            release: "Early Development",
            image: "/games/nebula-command.jpg"
        },
        {
            title: "Astera Blast",
            description: "The best Shoot'em up asteroid game",
            release: "Early Development",
            image: "/games/exo-pilgrim.jpg"
        },
        {
            title: "MARIS",
            description: "As MARIS-OS, an AI aboard Ares Station, you uncover a conspiricy. Manage the station, make choices, and decide who—or what—you'll become.",
            release: "Early Development",
            image: "/games/quantum-drift.jpg"
        }
    ];
</script>

<svelte:head>
    <title>Astera Interactive | Our Games</title>
    <meta name="description" content="Explore the immersive space games currently in development by Astera Interactive." />
</svelte:head>

<div class="page-container">
    <section class="games-section">
        <div class="section-header">
            <h1>GAMES IN DEVELOPMENT</h1>
            <div class="divider"></div>
            <p class="subtitle">Explore our upcoming titles that will transport you to the farthest reaches of the cosmos</p>
        </div>

        <div class="games-grid">
            {#each games as game}
                <div class="game-card">
                    <div class="game-image" style={`background-image: url('${game.image}')`}>
                        <div class="release-badge">{game.release}</div>
                    </div>
                    <div class="game-info">
                        <h2>{game.title}</h2>
                        <p>{game.description}</p>
                        <a href={`/games/${game.title.toLowerCase().replace(/\s+/g, '-')}`} class="learn-more">LEARN MORE →</a>
                    </div>
                </div>
            {/each}
        </div>
    </section>
</div>

<style>
    @import url('https://fonts.googleapis.com/css2?family=Orbitron:wght@400;700&family=Rajdhani:wght@300;500;700&display=swap');

    .page-container {
        padding: 80px 2rem 6rem;
        max-width: 1200px;
        margin: 0 auto;
    }

    /* Games Section */
    .games-section {
        padding: 2rem 0;
    }

    .section-header {
        text-align: center;
        margin-bottom: 4rem;
    }

    h1 {
        font-family: 'Orbitron', sans-serif;
        font-size: 2.8rem;
        color: #fff;
        margin-bottom: 1rem;
        letter-spacing: 2px;
    }

    .divider {
        height: 3px;
        width: 100px;
        background: linear-gradient(90deg, #41a0ff 0%, transparent 100%);
        margin: 0 auto 1.5rem;
    }

    .subtitle {
        font-size: 1.3rem;
        color: #a0a8c0;
        font-weight: 300;
        max-width: 600px;
        margin: 0 auto;
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

    h2 {
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

    /* Responsive */
    @media (max-width: 768px) {
        h1 {
            font-size: 2.2rem;
        }

        .subtitle {
            font-size: 1.1rem;
        }

        .games-grid {
            grid-template-columns: 1fr;
        }
    }
</style>