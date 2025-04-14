<footer class="space-footer">
  <div class="footer-content">
      <div class="footer-top">
          <div class="footer-brand">
              
              <h3>ASTERA INTERACTIVE</h3>
              <p>Pioneering the future of space gaming</p>
          </div>
        </div>

          <div class="footer-links">
              <div class="link-group">
                  <h4>EXPLORE</h4>
                  <a href="/games">Games</a>
                  <a href="/about">About Us</a>
                  <a href="/technology">Technology</a>
                  <a href="/careers">Careers</a>
              </div>

              <div class="link-group">
                  <h4>LEGAL</h4>
                  <a href="/privacy">Privacy Policy</a>
                  <a href="/terms">Terms of Service</a>
                  <a href="/cookies">Cookie Policy</a>
              </div>

              <div class="link-group">
                  <h4>CONNECT</h4>
                  <a href="https://twitter.com/asterainteractive">Twitter</a>
                  <a href="https://discord.gg/astera">Discord</a>
                  <a href="https://youtube.com/asterainteractive">YouTube</a>
                  <a href="mailto:contact@asterainteractive.com">Email</a>
              </div>
          </div>
      </div>
      

      <div class="footer-bottom">
        <p class="copyright">© 2157-{new Date().getFullYear()} Astera Interactive. All rights reserved.</p>
        <div class="back-to-top" on:click={() => window.scrollTo({ top: 0, behavior: 'smooth' })}>
            <span>RETURN TO ORBIT</span>
        </div>
    </div>
</footer>


<style>
  .space-footer {
      background: linear-gradient(180deg, #0a0e23 0%, #070914 100%);
      border-top: 1px solid rgba(65, 156, 255, 0.2);
      padding: 4rem 2rem 2rem;
      position: relative;
      overflow: hidden;
  }

  .space-footer::before {
      content: '';
      position: absolute;
      top: 0;
      left: 0;
      width: 100%;
      height: 1px;
      background: linear-gradient(90deg, transparent, rgba(65, 156, 255, 0.5), transparent);
      box-shadow: 0 0 10px rgba(65, 156, 255, 0.3);
  }

  .footer-content {
      max-width: 1200px;
      margin: 0 auto;
  }

  .footer-top {
      display: grid;
      grid-template-columns: 1fr 2fr;
      gap: 4rem;
      margin-bottom: 3rem;
  }

  .footer-brand {
      display: flex;
      flex-direction: column;
  }

  .footer-logo {
      width: 60px;
      height: auto;
      margin-bottom: 1rem;
  }

  .footer-brand h3 {
      font-family: 'Orbitron', sans-serif;
      color: #fff;
      margin: 0 0 0.5rem;
      font-size: 1.5rem;
      letter-spacing: 2px;
  }

  .footer-brand p {
      color: #a0a8c0;
      margin: 0;
      font-size: 0.9rem;
  }

  .footer-links {
      display: grid;
      grid-template-columns: repeat(3, 1fr);
      gap: 2rem;
  }

  .link-group {
      display: flex;
      flex-direction: column;
  }

  .link-group h4 {
      font-family: 'Orbitron', sans-serif;
      color: #fff;
      margin: 0 0 1.5rem;
      font-size: 1rem;
      letter-spacing: 1px;
  }

  .link-group a {
      color: #a0a8c0;
      text-decoration: none;
      margin-bottom: 1rem;
      font-size: 0.9rem;
      transition: all 0.3s ease;
  }

  .link-group a:hover {
      color: #41a0ff;
      transform: translateX(5px);
  }

  .footer-bottom {
      display: flex;
      justify-content: space-between;
      align-items: center;
      padding-top: 2rem;
      border-top: 1px solid rgba(65, 156, 255, 0.1);
  }

  .copyright {
      color: #6a7085;
      font-size: 0.8rem;
  }

  .back-to-top {
      display: flex;
      align-items: center;
      gap: 0.5rem;
      cursor: pointer;
      transition: all 0.3s ease;
  }

  .back-to-top span {
      color: #41a0ff;
      font-family: 'Orbitron', sans-serif;
      font-size: 0.8rem;
      letter-spacing: 1px;
  }

  .back-to-top:hover {
      transform: translateY(-3px);
  }

  @media (max-width: 768px) {
      .footer-top {
          grid-template-columns: 1fr;
          gap: 2rem;
      }

      .footer-links {
          grid-template-columns: 1fr;
          gap: 2rem;
      }

      .footer-bottom {
          flex-direction: column;
          gap: 1rem;
          text-align: center;
      }
  }
</style>