<template>
    <div class="services-page">
      <h1>Our Services</h1>
      <p>
        We offer a wide range of IT services to help businesses achieve their goals.
      </p>

      <!-- Service Cards -->
      <div class="services-grid">
        <div class="service" v-for="service in services" :key="service.id">
          <h2>{{ service.name }}</h2>
          <p>{{ service.description }}</p>
          <ul class="service-features">
            <li v-for="feature in service.features" :key="feature">{{ feature }}</li>
          </ul>
          <button @click="getQuote(service.name)" class="cta-btn">Get a Quote</button>
        </div>
      </div>
      
    </div>
    <hr>
    <!-- <ExampleServiceSections /> -->
  </template>
  
  <script>
// import ExampleServiceSections from '@/components/Servies/ExampleServiceSections.vue';

  export default {
    name: "ServicesPage",
    components: {
      // ExampleServiceSections,
    },
    data() {
      return {
        services: [
          {
            id: 1,
            name: "Managed IT Services",
            description: "24/7 monitoring and management of your IT infrastructure for smooth operations.",
            features: [
              "24/7 Monitoring",
              "Cloud Management",
              "Helpdesk Support",
              "Network Administration"
            ]
          },
          {
            id: 2,
            name: "Cybersecurity Solutions",
            description: "Protect your business from evolving cyber threats with advanced security solutions.",
            features: [
              "Threat Detection",
              "Data Encryption",
              "Vulnerability Assessments",
              "Firewall Management"
            ]
          },
          {
            id: 3,
            name: "Software Development",
            description: "Custom software and application development to meet your specific business needs.",
            features: [
              "Custom Software Development",
              "Mobile App Development",
              "API Integration",
              "Maintenance & Support"
            ]
          },
          {
            id: 4,
            name: "Cloud Migration",
            description: "Scalable cloud solutions to migrate your data and applications for better flexibility.",
            features: [
              "Cloud Strategy",
              "Data Migration",
              "Cloud Infrastructure Setup",
              "Post-Migration Support"
            ]
          }
        ]
      };
    },
    methods: {
      getQuote(serviceName) {
        alert(`Requesting a quote for ${serviceName}`);
      }
    }
  };
  </script>
  
  <style scoped>
  /* Main container for the services page */
  .services-page {
    max-width: 1200px;
    margin: 0 auto;
    padding: 40px 20px;
  }
  
  /* Heading */
  .services-page h1 {
    color: #333;
    font-size: 2.5rem;
    margin-bottom: 20px;
  }
  
  /* Description */
  
  .services-page p {
    color: #555;
    margin-bottom: 40px;
    line-height: 1.6;
  }
  
  /* Service section */
  .services-grid {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
    gap: 40px;
  }
  .service {
    margin-bottom: 40px;
    padding: 20px;
    background-color: #f9f9f9;
    border-radius: 10px;
    box-shadow: 0px 4px 8px rgba(0, 0, 0, 0.1);
  }
  
  .service h2 {
    color: #333;
    font-size: 1.8rem;
    margin-bottom: 10px;
  }
  
  .service p {
    color: #555;
    margin-bottom: 15px;
    line-height: 1.6;
  }
  
  .service-features {
    list-style-type: none;
    padding: 0;
    margin-bottom: 20px;
  }
  
  .service-features li {
    color: #333;
    padding: 5px 0;
    border-bottom: 1px solid #eee;
  }
  
  .cta-btn {
    padding: 10px 20px;
    background-color: #ff6b6b;
    color: white;
    border: none;
    border-radius: 25px;
    cursor: pointer;
    font-size: 1rem;
    transition: background-color 0.3s ease;
  }
  
  .cta-btn:hover {
    background-color: #ff5252;
  }
  
  /* Responsive adjustments */
  @media (max-width: 768px) {
    .service h2 {
      font-size: 1.6rem;
    }
  
    .cta-btn {
      width: 100%;
    }
  }
  </style>
  