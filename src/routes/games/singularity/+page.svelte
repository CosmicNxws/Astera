<script>
    
    const game = {
        description: "Datails soon",
        currentVersion: " Unreleased",
        features: [
            "Randomly Generated Levels - Gameplay is always diffrent",
            "10+ levels",
            "Simple and can run on nearly any computer",
            "Cool Music and sounds"
        ],
        updates: [
            {
                version: "0",
                date: "0",
                changes: [
                    "",
                    "",
                    ""
                ]
            },
            {
                version: "0",
                date: "0",
                changes: [
                    "",
                    "",
                    ""
                ]
            }
        ]
    };
</script>

<div class="page-container">
    <!-- 1. Hero Section -->
    <section class="hero-section">
        <div class="stars"></div>
        <div class="twinkling"></div>
        <div class="hero-content">
            <h1>SINGULARITY</h1>
            <div class="divider"></div>
            <p class="subtitle">The universe is your all-you-can-eat buffet! Guide your black hole to consume planets while avoiding nasty anti-stars and Those pesky humans in this gravity-powered arcade style game.</p>
        </div>
    </section>

 

    <!-- 3. Features Grid -->
    <section class="team-section">
        <div class="section-header">
            <h2>CORE FEATURES</h2>
            <div class="divider"></div>
        </div>
        <div class="team-grid">
            {#each game.features as feature, i}
                <div class="team-card">
                    <div class="space-box">
                        <div class="space-background"></div>
                        <div class="profile-circle">
                            <div class="initials">{i + 1}</div>
                        </div>
                    </div>
                    <div class="member-info">
                        <p class="bio">{feature}</p>
                    </div>
                </div>
            {/each}
        </div>
    </section>

    <!-- 4. Download Section -->
    <section class="about-section">
        <div class="section-content">
            <h2>GET SINGULARITY</h2>
            <div class="divider"></div>
            <p>Current Version: <strong>v{game.currentVersion}</strong></p>
            <div class="cta-buttons" style="margin-top: 2rem;">
                <a href="/download" class="cta-primary">DIRECT DOWNLOAD comming soon </a>
                <a href="https://store.steampowered.com" class="cta-secondary">N/A</a>
            </div>
        </div>
    </section>

    <!-- 5. Updates Section -->
    <section class="team-section" style="background: rgba(10,14,23,0.8)">
        <div class="section-header">
            <h2>UPDATE HISTORY</h2>
            <div class="divider"></div>
        </div>
        <div class="team-grid">
            {#each game.updates as update}
                <div class="team-card">
                    <div class="space-box">
                        <div class="space-background"></div>
                        <div class="profile-circle" style="background: linear-gradient(135deg, #41a0ff 0%, #2d6bff 100%)">
                            <div class="initials" style="color: white">v{update.version}</div>
                        </div>
                    </div>
                    <div class="member-info">
                        <h3>{update.date}</h3>
                        <ul style="color: #a0a8c0; padding-left: 1.2rem; margin-top: 0.5rem;">
                            {#each update.changes as change}
                                <li style="margin-bottom: 0.4rem;">{change}</li>
                            {/each}
                        </ul>
                    </div>
                </div>
            {/each}
        </div>
    </section>

   
</div>

<style>
    /* YOUR ORIGINAL CSS - COPIED VERBATIM */
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

    /* Space Box with Animated Stars */
    .space-box {
        height: 250px;
        position: relative;
        overflow: hidden;
    }

    .space-background {
        position: absolute;
        top: 0;
        left: 0;
        right: 0;
        bottom: 0;
        background: radial-gradient(ellipse at center, #0a0e17 0%, #000000 100%);
    }

    /* Star animations */
    @keyframes twinkle {
        0% { opacity: 0.2; transform: scale(0.8); }
        50% { opacity: 1; transform: scale(1.1); }
        100% { opacity: 0.2; transform: scale(0.8); }
    }

    @keyframes float {
        0% { transform: translateY(0) translateX(0); }
        50% { transform: translateY(-5px) translateX(5px); }
        100% { transform: translateY(0) translateX(0); }
    }

    .star {
        position: absolute;
        background-color: white;
        border-radius: 50%;
        animation: float 10s infinite ease-in-out;
    }

    .twinkling-star {
        position: absolute;
        width: 2px;
        height: 2px;
        background-color: white;
        border-radius: 50%;
        animation: twinkle 5s infinite, float 15s infinite ease-in-out;
        box-shadow: 0 0 5px 1px rgba(255, 255, 255, 0.8);
    }

    .deep-space-dots {
        position: absolute;
        top: 0;
        left: 0;
        right: 0;
        bottom: 0;
        background-image: 
            radial-gradient(white 1px, transparent 1px),
            radial-gradient(white 1px, transparent 1px);
        background-size: 30px 30px;
        background-position: 0 0, 15px 15px;
        opacity: 0.1;
    }

    /* Profile Circle */
    .profile-circle {
        position: absolute;
        top: 50%;
        left: 50%;
        transform: translate(-50%, -50%);
        width: 150px;
        height: 150px;
        border-radius: 50%;
        background-color: #1a1f3a;
        background-size: cover;
        background-position: center;
        border: 3px solid #41a0ff;
        box-shadow: 
            0 0 20px rgba(65, 156, 255, 0.5),
            0 0 40px rgba(65, 156, 255, 0.3) inset;
        z-index: 2;
        display: flex;
        align-items: center;
        justify-content: center;
    }

    .initials {
        font-family: 'Orbitron', sans-serif;
        font-size: 2.5rem;
        color: #41a0ff;
        font-weight: bold;
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
        font-size: 1.1rem;
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

        .profile-circle {
            width: 120px;
            height: 120px;
        }

        .initials {
            font-size: 2rem;
        }
    }
</style>