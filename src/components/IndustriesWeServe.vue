<template>
    <section class="industries-section">
      <h2 class="section-title">Industries We Serve</h2>
      <div class="industries-grid">
        <div 
          class="industry-card" 
          v-for="(industry, index) in industries" 
          :key="index"
          @mouseover="hoveredIndex = index"
          @mouseleave="hoveredIndex = null"
          :class="{ 'hovered': hoveredIndex === index }"
        >
          <div class="icon-container">
            <i :class="industry.icon"></i>
          </div>
          <p class="industry-label">{{ industry.name }}</p>
        </div>
      </div>
    </section>
  </template>
  
  <script>
  export default {
    name: "IndustriesWeServe",
    data() {
      return {
        hoveredIndex: null,
        industries: [
          { name: "Healthcare", icon: "fas fa-stethoscope" },
          { name: "Finance", icon: "fas fa-chart-line" },
          { name: "Education", icon: "fas fa-graduation-cap" },
          { name: "Retail", icon: "fas fa-store" },
          { name: "Manufacturing", icon: "fas fa-industry" },
          { name: "Technology", icon: "fas fa-laptop-code" },
          { name: "Transportation", icon: "fas fa-shipping-fast" },
          { name: "Hospitality", icon: "fas fa-concierge-bell" }
        ]
      };
    }
  };
  </script>
  
  <style scoped>
  /* Section Styling */
  .industries-section {
    padding: 60px 20px;
    background: #f9f9f9;
   

    text-align: center;
  }
  
  .section-title {
    font-size: 2rem;
    color: #333;
    margin-bottom: 40px;
    font-weight: bold;
  }
  
  /* Industries Grid */
  .industries-grid {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(150px, 1fr));
    gap: 20px;
    max-width: 1200px;
    margin: 0 auto;
  }
  
  /* Industry Card Styling */
  .industry-card {
    background-color: white;
    border-radius: 12px;
    padding: 20px;
    text-align: center;
    transition: all 0.3s ease-in-out;
    box-shadow: 0 4px 8px rgba(0, 0, 0, 0.1);
    cursor: pointer;
  }
  
  .icon-container {
    font-size: 2.5rem;
    color: #ff6b6b;
    margin-bottom: 15px;
    transition: transform 0.3s ease;
  }
  
  .industry-label {
    font-size: 1rem;
    color: #333;
    font-weight: 600;
    transition: color 0.3s;
  }
  
  /* Hover Effects */
  .industry-card:hover {
    transform: translateY(-10px);
    box-shadow: 0 6px 15px rgba(0, 0, 0, 0.2);
  }
  
  .industry-card.hovered .icon-container {
    transform: scale(1.2);
    color: #ff5252;
  }
  
  .industry-card.hovered .industry-label {
    color: #ff5252;
  }
  
  /* Responsive */
  @media (max-width: 768px) {
    .industries-grid {
      grid-template-columns: repeat(auto-fit, minmax(120px, 1fr));
    }
  
    .icon-container {
      font-size: 2rem;
    }
  
    .industry-label {
      font-size: 0.9rem;
    }
  }
  </style>
  