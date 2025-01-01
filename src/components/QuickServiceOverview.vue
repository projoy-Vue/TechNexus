<template>
  <section class="service-overview">
    <h2 class="section-title">Our Key Services</h2>
    <div class="service-cards">
      <!-- Managed IT Services Card -->
      <div class="service-card" v-for="service in services" :key="service.title">
        <i :class="service.icon"></i>
        <h3>{{ service.title }}</h3>
        <p>{{ service.description }}</p>
      </div>
    </div>
  </section>
</template>

<script>
export default {
  name: "QuickServiceOverview",
  data() {
    return {
      services: [
        {
          title: "Managed IT Services",
          icon: "fas fa-server", // Replace with CDN or local icons
          description:
            "24/7 monitoring, cloud management, and IT support to ensure business continuity.",
        },
        {
          title: "Cybersecurity Solutions",
          icon: "fas fa-shield-alt",
          description:
            "Advanced threat detection, data protection, and secure network services.",
        },
        {
          title: "Software Development",
          icon: "fas fa-code",
          description:
            "Custom software and app development tailored to your business needs.",
        },
        {
          title: "Cloud Migration",
          icon: "fas fa-cloud",
          description:
            "Scalable cloud solutions for seamless migration and optimized performance.",
        },
      ],
    };
  },
};
</script>

<style scoped>
/* Section Styling */
.service-overview {
  padding: 60px 30px;
  background: #f9f9f9;



  text-align: center;
}

.section-title {
  font-size: 2rem;
  color: #333;
  margin-bottom: 40px;
  font-weight: bold;
}

/* Service Cards Grid */
.service-cards {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(220px, 1fr));
  gap: 20px;
  justify-items: center;
  align-items: start;
}

.service-card {
  background-color: white;
  border-radius: 10px;
  box-shadow: 0 4px 12px rgba(0, 0, 0, 0.1);
  padding: 30px;
  transition: transform 0.3s ease, box-shadow 0.3s ease;
  text-align: center;
  /* width: 100%; */
  max-width: 300px;
  border: 1px solid #e1e4e8;
}

/* Icon Styling */
.service-card i {
  font-size: 2.5rem;
  color: #ff6b6b;
  margin-bottom: 20px;
}

/* Title and Description */
.service-card h3 {
  font-size: 1.25rem;
  margin-bottom: 15px;
  color: #333;
}

.service-card p {
  font-size: 1rem;
  color: #666;
  line-height: 1.5;
  margin-bottom: 10px;
}

/* Hover Effects */
.service-card:hover {
  transform: translateY(-5px);
  box-shadow: 0 6px 20px rgba(0, 0, 0, 0.15);
}

/* Responsive Design */
@media (max-width: 768px) {
  .service-cards {
    grid-template-columns: repeat(auto-fit, minmax(180px, 1fr));
  }

  .service-card {
    max-width: 240px;
  }
}
</style>
