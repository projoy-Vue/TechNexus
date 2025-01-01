<template>
  <div class="services-overview">
    <!-- Managed IT Services Section -->
    <div class="service-section">
      <h2>Managed IT Services</h2>
      <p>
        Includes 24/7 IT monitoring, remote support, and system administration.
      </p>
      <ul class="service-features">
        <li>Automatic backups</li>
        <li>Proactive maintenance</li>
        <li>Network management</li>
      </ul>
      <button class="cta-btn" @click="getQuote('Managed IT Services')">Get a Quote</button>
    </div>

    <!-- Cybersecurity Section -->
    <div class="service-section">
      <h2>Cybersecurity</h2>
      <p>Solutions Offered: Firewalls, encryption, ransomware defense.</p>
      <p class="value-prop">
        <strong>Value Proposition:</strong> "Protect your critical data and reduce cyber risk."
      </p>
      <button class="cta-btn" @click="getQuote('Cybersecurity')">Get a Quote</button>
    </div>

    <!-- Cloud Solutions Section -->
    <div class="service-section">
      <h2>Cloud Solutions</h2>
      <p>Benefits: Scalable storage, cloud migration, reduced costs.</p>
      <button class="cta-btn" @click="getQuote('Cloud Solutions')">Get a Quote</button>
    </div>

    <!-- Software Development Section -->
    <div class="service-section">
      <h2>Software Development</h2>
      <p>Solutions: Custom software, mobile apps, enterprise-level solutions.</p>
      <button class="cta-btn" @click="getQuote('Software Development')">Get a Quote</button>
    </div>
  </div>
</template>

<script>
export default {
  name: "ExampleServiceSections",
  methods: {
    getQuote(serviceName) {
      alert(`Requesting a quote for ${serviceName}`);
    }
  }
};
</script>

<style scoped>
/* Main container for services overview */
.services-overview {
  max-width: 1200px;
  margin: 0 auto;
  padding: 40px 20px;
}

/* Individual service section */
.service-section {
  margin-bottom: 40px;
  padding: 20px;
  background-color: #f9f9f9;
  border-radius: 10px;
  box-shadow: 0px 4px 8px rgba(0, 0, 0, 0.1);
}

/* Service titles */
.service-section h2 {
  color: #333;
  font-size: 1.8rem;
  margin-bottom: 10px;
}

/* Service description */
.service-section p {
  color: #555;
  margin-bottom: 15px;
  line-height: 1.6;
}

/* Value proposition style */
.value-prop {
  font-weight: bold;
  color: #333;
  margin-bottom: 15px;
}

/* Features list */
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

/* Call-to-action button style */
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
  .service-section h2 {
    font-size: 1.6rem;
  }

  .cta-btn {
    width: 100%;
  }
}
</style>
