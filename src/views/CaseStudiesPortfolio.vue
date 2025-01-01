<template>
    <div class="case-studies-portfolio">
      <h1 class="section-title">Featured Projects</h1>
      <div class="case-study" v-for="(project, index) in projects" :key="index">
        <div class="case-header">
          <h2>{{ project.title }}</h2>
        </div>
        <div class="case-content">
          <div class="case-item">
            <h3>Client Challenge</h3>
            <p>{{ project.challenge }}</p>
          </div>
          <div class="case-item">
            <h3>Our Solution</h3>
            <p>{{ project.solution }}</p>
          </div>
          <div class="case-item">
            <h3>Results</h3>
            <p>{{ project.results }}</p>
          </div>
          <div class="case-item">
            <h3>Technologies Used</h3>
            <ul>
              <li v-for="(tech, idx) in project.technologies" :key="idx">{{ tech }}</li>
            </ul>
          </div>
        </div>
      </div>
    </div>
  </template>
  
  <script>
  export default {
    name: "CaseStudiesPortfolio",
    data() {
      return {
        projects: [
          {
            title: "Healthcare System Optimization",
            challenge: "The client faced significant downtime and data integration issues between legacy systems.",
            solution: "We implemented a hybrid cloud infrastructure to streamline data flow, reducing downtime by 30%.",
            results: "Increased operational efficiency by 40%, reducing IT costs by 20%.",
            technologies: ["AWS", "Python", "Docker", "PostgreSQL"]
          },
          {
            title: "Finance App Development",
            challenge: "The client needed a custom finance app with secure real-time transaction tracking.",
            solution: "We built a secure, scalable mobile app with real-time tracking, encrypted transactions, and a user-friendly interface.",
            results: "Client saw a 50% increase in app usage and gained 10,000 new users in the first month.",
            technologies: ["React Native", "Node.js", "Azure", "MongoDB"]
          },
          {
            title: "Cloud Migration for E-Commerce",
            challenge: "The client's e-commerce platform was struggling with high traffic and performance issues.",
            solution: "We migrated the platform to a scalable cloud solution, handling peak traffic without latency.",
            results: "Reduced loading times by 45%, and ensured 99.9% uptime during peak shopping seasons.",
            technologies: ["Azure", "Python", "Kubernetes", "MySQL"]
          }
        ]
      };
    }
  };
  </script>
  
  <style scoped>
  .case-studies-portfolio {
    max-width: 1200px;
    margin: 0 auto;
    padding: 40px 20px;
    background-color: #f8f9fa;
    border-radius: 8px;
  }
  
  .section-title {
    text-align: center;
    font-size: 2.5rem;
    margin-bottom: 40px;
    color: #333;
  }
  
  .case-study {
    margin-bottom: 40px;
    padding: 20px;
    background-color: #fff;
    border-radius: 8px;
    box-shadow: 0 4px 12px rgba(0, 0, 0, 0.1);
  }
  
  .case-header h2 {
    font-size: 1.8rem;
    margin-bottom: 15px;
    color: #444;
  }
  
  .case-content {
    display: grid;
    grid-template-columns: 1fr;
    gap: 20px;
  }
  
  .case-item h3 {
    font-size: 1.2rem;
    color: #555;
  }
  
  .case-item p {
    color: #666;
    line-height: 1.6;
  }
  
  .case-item ul {
    list-style-type: none;
    padding: 0;
  }
  
  .case-item li {
    background-color: #eff3f6;
    padding: 8px 12px;
    margin-bottom: 5px;
    border-radius: 4px;
    color: #444;
  }
  
  /* Responsive Design */
  @media (min-width: 768px) {
    .case-content {
      grid-template-columns: 1fr 1fr;
    }
  }
  </style>
  