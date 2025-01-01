<template>
    <section class="contact-cta-section">
      <div class="cta-content">
        <h2 class="cta-title">Ready to transform your business?</h2>
        <p class="cta-subtitle">Contact us today and let's discuss how we can help you achieve your IT goals.</p>
        <a href="/contact" class="cta-button">Get in Touch</a>
      </div>
    </section>
  </template>
  
  <script>
  export default {
    name: "ContactCTA"
  };
  </script>
  
  <style scoped>
  /* Contact CTA Section Styling */
  .contact-cta-section {
    padding: 60px 20px;
    background-color: #1f2937; /* Dark background color for contrast */
    color: #fff;
    text-align: center;
  }
  
  .cta-content {
    max-width: 800px;
    margin: 0 auto;
  }
  
  .cta-title {
    font-size: 2.5rem;
    font-weight: 700;
    margin-bottom: 20px;
    color: #ff6b6b; /* Highlighted title color */
  }
  
  .cta-subtitle {
    font-size: 1.2rem;
    margin-bottom: 40px;
    color: #d1d5db; /* Light gray subtitle for a softer tone */
  }
  
  .cta-button {
    padding: 15px 40px;
    background-color: #ff6b6b;
    color: white;
    font-size: 1.1rem;
    font-weight: 600;
    text-transform: uppercase;
    text-decoration: none;
    border-radius: 30px;
    transition: background-color 0.3s ease;
  }
  
  .cta-button:hover {
    background-color: #ff5252;
    transition: background-color 0.3s ease;
  }
  
  /* Responsive */
  @media (max-width: 768px) {
    .cta-title {
      font-size: 2rem;
    }
  
    .cta-subtitle {
      font-size: 1rem;
    }
  
    .cta-button {
      padding: 12px 30px;
      font-size: 1rem;
    }
  }
  </style>
  