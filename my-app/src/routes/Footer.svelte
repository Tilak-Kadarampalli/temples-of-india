<script>
  import logo from '$lib/images/logo.png';
  import facebook from '$lib/images/facebook-logo.png';
  import twitter from '$lib/images/twitter-logo.png';
  import instagram from '$lib/images/Instagram-logo.png';
  import linkedin from '$lib/images/linkedin-logo.png';

  </script>
  
  <footer>
    <div class="footer-container">
      <!-- First Column -->
      <div class="footer-column">
        <div class="temples-logo">
          <img src={logo} alt="Logo" />
          <span>Temples of India</span>
        </div>
        <p class="tagline">World's largest Hindu Temples Portal</p>
      </div>
      <!-- Second Column -->
      <div class="footer-column">
        <h3>Quick Links</h3>
        <ul>
          <li><a href="/">Home</a></li>
          <li><a href="/about-us">About Us</a></li>
          <li><a href="/nearby-temples">Nearby Temples</a></li>
          <li><a href="/download-app">Download App</a></li>
          <li><a href="/donate">Donate to Us</a></li>
        </ul>
      </div>
      <!-- Third Column -->
      <div class="footer-column">
        <h3>Explore</h3>
        <ul>
          <li><a href="/search-temples">Search Temples</a></li>
          <li><a href="/watch-video">Watch Video</a></li>
          <li><a href="/disclaimer">Disclaimer</a></li>
          <li><a href="/blog">Our Blog</a></li>
          <li><a href="/donate-dharma">Donate for Dharma</a></li>
        </ul>
      </div>
      <!-- Fourth Column -->
      <div class="footer-column">
        <div class="social-icons">
          <a href="https://facebook.com"><img src={facebook} alt="Facebook" /></a>
          <a href="https://twitter.com"><img src={twitter} alt="Twitter" /></a>
          <a href="https://instagram.com"><img src={instagram} alt="Instagram" /></a>
          <a href="https://linkedin.com"><img src={linkedin} alt="LinkedIn" /></a>
        </div>
      </div>
    </div>
    <div class="copyright">
      ©Temples of India 2020-2023 | Email: <a href="mailto:contact@templesofindia.org">contact@templesofindia.org</a>
    </div>
  </footer>
  
  <style>
    .footer-container {
      display: flex;
      justify-content: space-between;
      padding: 20px;
      background-color: #ffe240;
      color: #a50740;
    }
  
    .footer-column {
      display: flex;
      flex-direction: column;
    }
  
    .temples-logo {
      display: flex;
      align-items: center;
    }
  
    .temples-logo img {
      margin-right: 10px;
    }
  
    .tagline {
      font-style: italic;
    }
  
    .footer-column h3 {
      margin-bottom: 10px;
    }
  
    .footer-column ul {
      list-style: none;
      padding: 0;
    }
  
    .footer-column ul li a {
      color: #a50740;
      text-decoration: none;
    }
  
    .social-icons a img {
      width: 24px;
      height: 24px;
      margin-right: 10px;
    }
  
    .copyright {
      text-align: center;
      padding: 10px;
      background-color: #ffc240; 
      color: #a50740;
      font-size: 0.8em;
    }
  
    .copyright a {
      color: #a50740;
      text-decoration: none;
    }

    @media (max-width: 768px) {
    .footer-container {
      flex-direction: column;
      align-items: flex-start;
    }

    .footer-column {
      width: 100%;
      max-width: 300px;
      align-items: flex-start;
      
    }

    .temples-logo {
      justify-content: flex-start;
    }

    .social-icons {
      justify-content: flex-start;
    }

    .social-icons a img {
      width: 32px;
      height: 32px;
    }
  }
  </style>
  