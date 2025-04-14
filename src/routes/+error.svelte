<script>
  import { page } from '$app/stores';
  
  // Fun space-themed error messages
  const errorMessages = [
      "Huston we have a problem!!",
      "Navigation systems offline!",
      "Propulsion systems malfunction!"
  ];
  
  // Random error message
  const randomMessage = errorMessages[Math.floor(Math.random() * errorMessages.length)];
  
  // Fun astronaut ASCII art
  const astronaut = `
         ___
       /     \\
      | O   O |
      |   ∆   |
       \\  -  /
        \\___/
  `;
</script>

<svelte:head>
  <title>Astera Interactive | Navigation Error</title>
  <meta name="description" content="You've encountered a cosmic anomaly in navigation" />
</svelte:head>

<div class="error-container">
  <section class="error-hero">
      <div class="stars"></div>
      <div class="twinkling"></div>
      <div class="comet"></div>
      <div class="pulsar"></div>
      
      <div class="error-content">
          <div class="error-code">404</div>
          <h1>LOST IN SPACE</h1>
          <div class="divider"></div>
          <p class="error-message">{randomMessage}</p>
          <pre class="ascii-art">{astronaut}</pre>
          <p class="error-description">The page you're looking for has either been swallowed by a black hole or never existed in this dimension.</p>
          
          <div class="error-actions">
              <a href="/" class="cta-primary">
                  <span class="icon">🚀</span> RETURN TO HOME
              </a>
              <a href="/games" class="cta-secondary">
                  <span class="icon">🎮</span> EXPLORE GAMES
              </a>
          </div>
          
          <div class="error-tech">
              <p class="debug">{$page.url.pathname} not found</p>
              <div class="scanlines"></div>
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
      height: 90vh;
  }

  .error-container {
      height: 70vh;
      position: relative;
  }

  /* Hero Section */
  .error-hero {
      height: 100%;
      position: relative;
      display: flex;
      align-items: center;
      justify-content: center;
      overflow: hidden;
      background: radial-gradient(ellipse at bottom, #1B2735 0%, #090A0F 100%);
      text-align: center;
  }

  .error-content {
      z-index: 10;
      padding: 2rem;
      max-width: 800px;
      position: relative;
  }

  .error-code {
      font-family: 'Orbitron', sans-serif;
      font-size: 8rem;
      font-weight: 700;
      color: rgba(65, 156, 255, 0.2);
      line-height: 1;
      margin-bottom: -2rem;
      position: relative;
      animation: pulse 2s infinite alternate;
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
      position: relative;
  }

  .error-message {
      font-family: 'Orbitron', sans-serif;
      font-size: 1.8rem;
      color: #ff4d7d;
      margin-bottom: 2rem;
      text-shadow: 0 0 10px rgba(255, 77, 125, 0.5);
  }

  .ascii-art {
      color: #41a0ff;
      font-size: 0.8rem;
      line-height: 1.3;
      margin: 1rem auto;
      white-space: pre;
      text-shadow: 0 0 10px rgba(65, 156, 255, 0.5);
  }

  .error-description {
      font-size: 1.2rem;
      color: #a0a8c0;
      margin-bottom: 3rem;
      max-width: 600px;
      margin-left: auto;
      margin-right: auto;
  }

  .error-actions {
      display: flex;
      gap: 1.5rem;
      justify-content: center;
      margin-bottom: 3rem;
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
      display: flex;
      align-items: center;
      gap: 0.5rem;
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

  .icon {
      font-size: 1.2rem;
  }

  .error-tech {
      margin-top: 3rem;
      position: relative;
      padding: 1rem;
      border: 1px solid rgba(65, 156, 255, 0.2);
      border-radius: 4px;
      background: rgba(10, 14, 23, 0.5);
      max-width: 500px;
      margin-left: auto;
      margin-right: auto;
  }

  .debug {
      font-family: monospace;
      color: #a0a8c0;
      font-size: 0.9rem;
      margin: 0;
      position: relative;
      z-index: 2;
  }

  .scanlines {
      position: absolute;
      top: 0;
      left: 0;
      width: 100%;
      height: 100%;
      background: linear-gradient(
          to bottom,
          rgba(65, 156, 255, 0.03) 0%,
          rgba(65, 156, 255, 0.1) 50%,
          rgba(65, 156, 255, 0.03) 100%
      );
      background-size: 100% 4px;
      pointer-events: none;
      animation: scanline 8s linear infinite;
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

  /* Comet Animation */
  .comet {
      position: absolute;
      top: 10%;
      right: 10%;
      width: 6px;
      height: 6px;
      border-radius: 50%;
      background: #fff;
      box-shadow: 0 0 20px 10px rgba(255, 255, 255, 0.5);
      opacity: 0;
      z-index: 2;
      animation: comet 20s linear infinite;
  }

  /* Pulsar Animation */
  .pulsar {
      position: absolute;
      bottom: 20%;
      left: 15%;
      width: 10px;
      height: 10px;
      border-radius: 50%;
      background: rgba(65, 156, 255, 0.8);
      box-shadow: 0 0 0 0 rgba(65, 156, 255, 0.7);
      opacity: 0.7;
      z-index: 2;
      animation: pulsar 3s infinite;
  }

  /* Animations */
  @keyframes pulse {
      0% { opacity: 0.7; }
      100% { opacity: 0.3; }
  }

  @keyframes glitch {
      0% { transform: translate(0); }
      20% { transform: translate(-3px, 3px); }
      40% { transform: translate(-3px, -3px); }
      60% { transform: translate(3px, 3px); }
      80% { transform: translate(3px, -3px); }
      100% { transform: translate(0); }
  }

  @keyframes scanline {
      0% { background-position: 0 0; }
      100% { background-position: 0 100%; }
  }

  @keyframes comet {
      0% {
          transform: translateX(0) translateY(0);
          opacity: 1;
      }
      50% {
          transform: translateX(-300px) translateY(150px);
          opacity: 1;
      }
      100% {
          transform: translateX(-600px) translateY(300px);
          opacity: 0;
      }
  }

  @keyframes pulsar {
      0% {
          box-shadow: 0 0 0 0 rgba(65, 156, 255, 0.7);
      }
      70% {
          box-shadow: 0 0 0 30px rgba(65, 156, 255, 0);
      }
      100% {
          box-shadow: 0 0 0 0 rgba(65, 156, 255, 0);
      }
  }

  /* Responsive */
  @media (max-width: 768px) {
      .error-code {
          font-size: 5rem;
      }

      h1 {
          font-size: 2.5rem;
      }

      .error-message {
          font-size: 1.4rem;
      }

      .error-actions {
          flex-direction: column;
          gap: 1rem;
      }

      .error-description {
          font-size: 1rem;
      }
  }
</style>