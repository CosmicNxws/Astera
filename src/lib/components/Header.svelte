<header class="space-header">
    <div class="header-content">
        <div class="logo-container">
            
            <h1>ASTERA INTERACTIVE</h1>
        </div>
        <nav class="nav-menu">
            <a href="/" class="nav-link active">HOME</a>
            <a href="/games" class="nav-link">GAMES</a>
            <a href="/about" class="nav-link">ABOUT</a>
            <a href="/careers" class="nav-link">CAREERS</a>
            <a href="/contact" class="nav-link">CONTACT</a>
        </nav>
        <div class="hamburger">
            <div class="line"></div>
            <div class="line"></div>
            <div class="line"></div>
        </div>
    </div>
</header>

<style>
    .space-header {
        background: linear-gradient(90deg, #0a0e23 0%, #1a1f3a 100%);
        border-bottom: 1px solid rgba(65, 156, 255, 0.2);
        box-shadow: 0 0 20px rgba(65, 156, 255, 0.1);
        position: fixed;
        width: 100%;
        top: 0;
        z-index: 1000;
        backdrop-filter: blur(5px);
    }

    .header-content {
        display: flex;
        justify-content: space-between;
        align-items: center;
        max-width: 1200px;
        margin: 0 auto;
        padding: 1rem 2rem;
    }

    .logo-container {
        display: flex;
        align-items: center;
        gap: 1rem;
    }

    .logo {
        height: 40px;
        width: auto;
    }

    h1 {
        color: #fff;
        font-family: 'Orbitron', sans-serif;
        font-size: 1.5rem;
        letter-spacing: 2px;
        margin: 0;
        text-shadow: 0 0 10px rgba(65, 156, 255, 0.5);
    }

    .nav-menu {
        display: flex;
        gap: 2rem;
    }

    .nav-link {
        color: #a0a8c0;
        text-decoration: none;
        font-family: 'Rajdhani', sans-serif;
        font-weight: 600;
        font-size: 1rem;
        letter-spacing: 1px;
        text-transform: uppercase;
        transition: all 0.3s ease;
        position: relative;
    }

    .nav-link:hover, .nav-link.active {
        color: #41a0ff;
        text-shadow: 0 0 10px rgba(65, 156, 255, 0.7);
    }

    .nav-link.active::after {
        content: '';
        position: absolute;
        bottom: -8px;
        left: 0;
        width: 100%;
        height: 2px;
        background: #41a0ff;
        box-shadow: 0 0 10px #41a0ff;
    }

    .hamburger {
        display: none;
        flex-direction: column;
        gap: 5px;
        cursor: pointer;
    }

    .hamburger .line {
        width: 25px;
        height: 2px;
        background: #fff;
        transition: all 0.3s ease;
    }

    @media (max-width: 768px) {
        .nav-menu {
            display: none;
        }

        .hamburger {
            display: flex;
        }
    }
</style>