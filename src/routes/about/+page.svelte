<script>
    const team = [
        {
            name: "Dr. Elara Voss",
            role: "Founder & Creative Director",
            bio: "Visionary astrophysicist turned game designer, Elara brings scientific rigor to our cosmic adventures.",
            image: "/team/elara-voss.jpg"
        },
        {
            name: "Kieran Rho",
            role: "Lead Developer",
            bio: "Quantum computing expert who builds the impossible. Architect of the ASTERIA engine.",
            image: "/team/kieran-rho.jpg"
        },
        {
            name: "Nyx Orion",
            role: "Art Director",
            bio: "Concept artist who paints galaxies before breakfast. Creates our signature neo-cosmic aesthetic.",
            image: "/team/nyx-orion.jpg"
        },
        {
            name: "Dr. Soren Maris",
            role: "Narrative Designer",
            bio: "Exoplanet researcher who writes stories that span solar systems. Our resident worldbuilder.",
            image: "/team/soren-maris.jpg"
        },
        {
            name: "Juno Cade",
            role: "Sound Designer",
            bio: "Crafts audio landscapes that make vacuum feel alive. Records actual space probe telemetry for samples.",
            image: "/team/juno-cade.jpg"
        },
        {
            name: "Vega Quinn",
            role: "Community Director",
            bio: "Keeps our connection to Earth while we're lost in the stars. Builds bridges between players and devs.",
            image: "/team/vega-quinn.jpg"
        }
    ];
</script>

<svelte:head>
    <title>Astera Interactive | Our Team</title>
    <meta name="description" content="Meet the visionary team behind Astera Interactive's immersive space gaming experiences." />
</svelte:head>

<div class="page-container">
    <section class="hero-section">
        <div class="hero-content">
            <h1>MEET THE CREW</h1>
            <div class="divider"></div>
            <p class="subtitle">The brilliant minds charting our course through the gaming cosmos</p>
        </div>
        <div class="stars"></div>
        <div class="twinkling"></div>
    </section>

    <section class="about-section">
        <div class="section-content">
            <h2>OUR MISSION</h2>
            <div class="divider"></div>
            <p>Founded in 2025, Astera Interactive exists to push the boundaries of space exploration gaming.  </p>
            <p>TBD</p>
        </div>
    </section>

    <section class="team-section">
        <div class="section-header">
            <h2>KEY PERSONNEL</h2>
            <div class="divider"></div>
        </div>

        <div class="team-grid">
            {#each team as member}
                <div class="team-card">
                    <div class="member-image" style={`background-image: url('${member.image}')`}></div>
                    <div class="member-info">
                        <h3>{member.name}</h3>
                        <p class="role">{member.role}</p>
                        <p class="bio">{member.bio}</p>
                        <div class="social-links">
                            <a href="#" aria-label={`${member.name}'s profile`}>🌌</a>
                            <a href="#" aria-label={`Contact ${member.name}`}>📡</a>
                        </div>
                    </div>
                </div>
            {/each}
        </div>
    </section>

    <section class="cta-section">
        <h2>READY TO EXPLORE WITH US?</h2>
        <div class="divider"></div>
        <p>Join our crew of interstellar pioneers and be the first to experience our cosmic adventures.</p>
        <div class="cta-buttons">
            <a href="/games" class="cta-primary">SEE OUR GAMES</a>
            <a href="#" class="cta-secondary">CAREERS</a>
        </div>
    </section>
</div>

<style>
    @import url('https://fonts.googleapis.com/css2?family=Orbitron:wght@400;700&family=Rajdhani:wght@300;500;700&display=swap');

    .page-container {
        padding-top: 80px;
        color: #e0e0e0;
        font-family: 'Rajdhani', sans-serif;
        max-width: 1200px;
        margin: 0 auto;
    }

    /* Hero Section */
    .hero-section {
        height: 50vh;
        min-height: 500px;
        position: relative;
        display: flex;
        align-items: center;
        justify-content: center;
        overflow: hidden;
        background: radial-gradient(ellipse at bottom, #1B2735 0%, #090A0F 100%);
        text-align: center;
    }

    .hero-content {
        z-index: 10;
        padding: 0 2rem;
        max-width: 800px;
    }

    h1 {
        font-family: 'Orbitron', sans-serif;
        font-size: 3.5rem;
        margin-bottom: 1.5rem;
        color: #fff;
        text-shadow: 0 0 20px rgba(65, 156, 255, 0.7);
        letter-spacing: 3px;
    }

    .divider {
        height: 3px;
        width: 100px;
        background: linear-gradient(90deg, #41a0ff 0%, transparent 100%);
        margin: 0 auto 2rem;
    }

    .subtitle {
        font-size: 1.5rem;
        color: #a0a8c0;
        font-weight: 300;
        max-width: 600px;
        margin: 0 auto;
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

    /* About Section */
    .about-section {
        padding: 6rem 2rem;
        text-align: center;
    }

    .section-content {
        max-width: 800px;
        margin: 0 auto;
    }

    h2 {
        font-family: 'Orbitron', sans-serif;
        font-size: 2.5rem;
        color: #fff;
        margin-bottom: 1.5rem;
        letter-spacing: 2px;
    }

    .about-section p {
        color: #a0a8c0;
        margin-bottom: 1.5rem;
        line-height: 1.7;
        font-size: 1.1rem;
    }

    /* Team Section */
    .team-section {
        padding: 4rem 2rem;
        background: linear-gradient(180deg, rgba(10, 14, 23, 0) 0%, rgba(26, 31, 58, 0.7) 100%);
    }

    .section-header {
        text-align: center;
        margin-bottom: 4rem;
    }

    .team-grid {
        display: grid;
        grid-template-columns: repeat(auto-fit, minmax(350px, 1fr));
        gap: 2rem;
    }

    .team-card {
        background: rgba(26, 31, 58, 0.6);
        border-radius: 8px;
        overflow: hidden;
        transition: transform 0.3s ease, box-shadow 0.3s ease;
        border: 1px solid rgba(65, 156, 255, 0.2);
        display: flex;
        flex-direction: column;
    }

    .team-card:hover {
        transform: translateY(-10px);
        box-shadow: 0 10px 30px rgba(65, 156, 255, 0.2);
    }

    .member-image {
        height: 250px;
        background-size: cover;
        background-position: center;
    }

    .member-info {
        padding: 1.5rem;
        flex-grow: 1;
        display: flex;
        flex-direction: column;
    }

    h3 {
        font-family: 'Orbitron', sans-serif;
        font-size: 1.5rem;
        margin: 0 0 0.5rem;
        color: #fff;
    }

    .role {
        color: #41a0ff;
        font-weight: 700;
        margin-bottom: 1rem;
        font-size: 0.9rem;
    }

    .bio {
        color: #a0a8c0;
        margin-bottom: 1.5rem;
        line-height: 1.6;
        flex-grow: 1;
    }

    .social-links {
        display: flex;
        gap: 1rem;
    }

    .social-links a {
        color: #41a0ff;
        text-decoration: none;
        font-size: 1.2rem;
        transition: all 0.3s ease;
    }

    .social-links a:hover {
        color: #fff;
        text-shadow: 0 0 10px rgba(65, 156, 255, 0.7);
    }

    /* CTA Section */
    .cta-section {
        padding: 6rem 2rem;
        text-align: center;
    }

    .cta-section p {
        color: #a0a8c0;
        max-width: 600px;
        margin: 0 auto 2rem;
        font-size: 1.1rem;
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

    /* Responsive */
    @media (max-width: 768px) {
        h1 {
            font-size: 2.5rem;
        }

        h2 {
            font-size: 2rem;
        }

        .subtitle {
            font-size: 1.2rem;
        }

        .hero-section {
            height: 50vh;
            min-height: 400px;
        }

        .team-grid {
            grid-template-columns: 1fr;
        }

        .cta-buttons {
            flex-direction: column;
            gap: 1rem;
        }
    }
</style>