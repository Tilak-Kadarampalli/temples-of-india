<script>
  import logo from '$lib/images/logo.png';
</script>

<nav>
  <div class="logo">
    <img src={logo} alt="Logo" />
    <span>Temples of India</span>
  </div>
  <ul class="nav-links">
    <li><a href="/">Home</a></li>
    <li class="search-link"><a href="/search">Search</a></li>
    <li><a href="/nearby-temples">Nearby Temples</a></li>
    <li><a href="/add-temples">Add Temples</a></li>
    <li><a href="/about-us">About Us</a></li>
    <li><a href="/login">Login</a></li>
  </ul>
</nav>

<style>
  nav {
    display: flex;
    justify-content: space-between;
    align-items: center;
    background-color: #ffffff;
    color: #000000;
    
    font-size: 34px;
  }
  .logo {
    display: flex;
    align-items: center;
  }
  .logo img {
    height: 50px; /* Adjust size as needed */
  }
  .logo span {
    font-family: 'Playfair Display';
    margin-left: 10px;
    font-size: 36px; /* Adjust size as needed */
  }
  .nav-links {
    list-style: none;
    display: flex;
  
    font-size: 16px;;
  }
  .nav-links li {
    padding: 0 20px; /* Adjust spacing as needed */
  }
  .nav-links li a {
    text-decoration: none;
    color: black;
    transition: color 0.3s ease;
  }
  .nav-links li a:hover {
    color: grey;
  }

  /* Responsive styles */
  @media (max-width: 768px) {
    .nav-links li:not(.search-link) {
      display: none;
    }
  }
</style>
