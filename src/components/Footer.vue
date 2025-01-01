<template>
    <footer class="footer">
      <div class="container">
        <div class="footer-columns">
          <!-- Column 1: Quick Links -->
          <div class="footer-column">
            <h4>Quick Links</h4>
            <ul class="footer-links">
              <li><a href="#">Home</a></li>
              <li><a href="#">Services</a></li>
              <li><a href="#">About Us</a></li>
              <li><a href="#">Contact Us</a></li>
              <li><a href="#">Careers</a></li>
              <li><a href="#">FAQs</a></li>
              <li><a href="#">Privacy Policy</a></li>
              <li><a href="#">Terms of Service</a></li>
            </ul>
            <a class="cta-btn" href="#">Get a Free Quote</a>
          </div>
  
          <!-- Column 2: Services -->
          <div class="footer-column">
            <h4>Services</h4>
            <ul class="footer-links">
              <li><a href="#">Managed IT Services</a></li>
              <li><a href="#">Cybersecurity</a></li>
              <li><a href="#">Cloud Solutions</a></li>
              <li><a href="#">Software Development</a></li>
              <li><a href="#">IT Consulting</a></li>
            </ul>
          </div>
  
          <!-- Column 3: Resources -->
          <div class="footer-column">
            <h4>Resources</h4>
            <ul class="footer-links">
              <li><a href="#">Latest IT Insights</a></li>
              <li><a href="#">Cybersecurity Tips</a></li>
              <li><a href="#">Cloud Migration Guide</a></li>
              <li><a href="#">Whitepapers</a></li>
              <li><a href="#">Case Studies</a></li>
            </ul>
            <div class="newsletter-signup">
              <h4>Subscribe to our Newsletter</h4>
              <input type="email" placeholder="Your email" />
              <button>Subscribe</button>
            </div>
          </div>
  
          <!-- Column 4: Contact Info & Social Media -->
          <div class="footer-column">
            <h4>Contact Info</h4>
            <p>TechNexus Solutions, 123 IT Park Ave, City, Country</p>
            <p>Call Us: +123 456 7890</p>
            <p>Email Us: <a href="mailto:info@technexus.com">info@technexus.com</a></p>
  
            <div class="social-media">
              <h4>Follow Us</h4>
              <a href="#"><i class="fab fa-linkedin"></i></a>
              <a href="#"><i class="fab fa-twitter"></i></a>
              <a href="#"><i class="fab fa-facebook"></i></a>
              <a href="#"><i class="fab fa-instagram"></i></a>
            </div>
  
            <a class="live-chat" href="#">Live Chat</a>
          </div>
        </div>
  
        <!-- Bottom Bar -->
        <div class="bottom-bar">
          <p>© 2024 TechNexus Solutions. All Rights Reserved.</p>
          <ul class="footer-bottom-links">
            <li><a href="#">Privacy Policy</a></li>
            <li><a href="#">Terms of Service</a></li>
          </ul>
        </div>
      </div>
    </footer>
  </template>
  
  <script>
  export default {
    name: "Footer",
  };
  </script>
  
  <style scoped>
  /* Footer Section */
  .footer {
    background-color: #1f2937;
    color: #d1d5db;
    padding: 40px 20px;
    border-top: 1px solid #344055;
  }
  
  .container {
    max-width: 1200px;
    margin: 0 auto;
  }
  
  .footer-columns {
    display: flex;
    flex-wrap: wrap;
    justify-content: space-between;
    gap: 40px;
  }
  
  .footer-column {
    flex: 1;
    min-width: 220px;
  }
  
  .footer-column h4 {
    color: #ff6b6b;
    font-size: 1.2rem;
    margin-bottom: 15px;
  }
  
  .footer-links {
    list-style: none;
    padding: 0;
    margin: 0;
  }
  
  .footer-links li {
    margin-bottom: 10px;
  }
  
  .footer-links li a {
    color: #d1d5db;
    text-decoration: none;
    transition: color 0.3s ease;
  }
  
  .footer-links li a:hover {
    color: #ff6b6b;
  }
  
  .cta-btn {
    display: inline-block;
    margin-top: 20px;
    padding: 10px 20px;
    background-color: #ff6b6b;
    color: white;
    text-decoration: none;
    border-radius: 25px;
    transition: background-color 0.3s ease;
  }
  
  .cta-btn:hover {
    background-color: #ff5252;
  }
  
  .newsletter-signup {
    margin-top: 20px;
  }
  
  .newsletter-signup input {
    padding: 10px;
    margin-right: 10px;
    border-radius: 5px;
    border: none;
    width: 90%;
  }
  
  .newsletter-signup button {
    margin-top: 10px;
    padding: 10px 20px;
    background-color: #ff6b6b;
    color: white;
    border: none;
    border-radius: 5px;
    cursor: pointer;
    transition: background-color 0.3s ease;
    width: 98%;
  }
  
  .newsletter-signup button:hover {
    background-color: #ff5252;
  }
  
  /* Contact Info & Social Media */
  .social-media {
    margin-top: 20px;
  }
  
  .social-media a {
    color: white;
    margin-right: 10px;
    font-size: 1.5rem;
    transition: color 0.3s ease;
  }
  
  .social-media a:hover {
    color: #ff6b6b;
  }
  
  .live-chat {
    display: inline-block;
    margin-top: 20px;
    color: #ff6b6b;
    text-decoration: none;
    font-weight: bold;
    transition: color 0.3s ease;
  }
  
  .live-chat:hover {
    color: #ff5252;
  }
  
  /* Bottom Bar */
  .bottom-bar {
    margin-top: 40px;
    padding-top: 20px;
    border-top: 1px solid #374151;
    display: flex;
    justify-content: space-between;
    flex-wrap: wrap;
    color: #9ca3af;
    font-size: 0.9rem;
  }
  
  .footer-bottom-links {
    list-style: none;
    display: flex;
    gap: 15px;
  }
  
  .footer-bottom-links li a {
    color: #9ca3af;
    text-decoration: none;
  }
  
  .footer-bottom-links li a:hover {
    color: #ff6b6b;
  }
  
  /* Responsive Design */
  @media (max-width: 768px) {
    .footer-columns {
      flex-direction: column;
      text-align: center;
    }
  
    .footer-column {
      min-width: 100%;
    }
  
    .newsletter-signup input {
      width: 100%;
      margin-bottom: 10px;
    }
  
    .bottom-bar {
      flex-direction: column;
      text-align: center;
    }
  }
  </style>
  