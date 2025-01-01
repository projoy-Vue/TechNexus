<template>
  <section class="testimonials-section">
    <h2 class="section-title">What Our Clients Say</h2>
    <div class="carousel">
      <div
        class="testimonial"
        v-for="(testimonial, index) in testimonials"
        :key="testimonial.company"
        :class="{ 'active': currentIndex === index }"
        :style="{ transform: `translateX(${-currentIndex * 100}%)` }"
      >
        <div class="testimonial-content">
          <img :src="testimonial.logo" alt="Company Logo" class="company-logo" />
          <p class="review">{{ testimonial.review }}</p>
          <h3 class="client-name">{{ testimonial.name }}</h3>
          <p class="company">{{ testimonial.company }}</p>
        </div>
      </div>
    </div>

    <!-- Carousel Controls -->
    <div class="carousel-controls">
      <button @click="prev" class="prev-btn"><i class="fas fa-chevron-left"></i></button>
      <button @click="next" class="next-btn"><i class="fas fa-chevron-right"></i></button>
    </div>

    <!-- Dots Navigation -->
    <div class="carousel-dots">
      <span
        v-for="(testimonial, index) in testimonials"
        :key="index"
        :class="{ 'active-dot': currentIndex === index }"
        @click="currentIndex = index"
      ></span>
    </div>
  </section>
</template>

<script>
export default {
  name: "TestimonialsCarousel",
  data() {
    return {
      currentIndex: 0,
      testimonials: [
        {
          name: "Jane Doe",
          company: "Tech Innovators Inc.",
          logo: "https://via.placeholder.com/100x50", // Example logo URL
          review:
            "TechNexus helped us streamline our IT operations, leading to increased efficiency and growth.",
        },
        {
          name: "John Smith",
          company: "Global Solutions",
          logo: "https://via.placeholder.com/100x50",
          review:
            "Their cybersecurity services have given us peace of mind. We're more secure than ever.",
        },
        {
          name: "Emily Johnson",
          company: "Cloud Ventures",
          logo: "https://via.placeholder.com/100x50",
          review:
            "The cloud migration was seamless, and now we have scalable solutions that fit our business needs.",
        },
        {
          name: "Michael Brown",
          company: "App Masters",
          logo: "https://via.placeholder.com/100x50",
          review:
            "Their software development team built us a custom solution that transformed how we operate.",
        },
      ],
    };
  },
  methods: {
    next() {
      this.currentIndex = (this.currentIndex + 1) % this.testimonials.length;
    },
    prev() {
      this.currentIndex =
        (this.currentIndex - 1 + this.testimonials.length) %
        this.testimonials.length;
    },
  },
};
</script>

<style scoped>
/* Section Styling */
.testimonials-section {
  padding: 60px 30px;
  background: #f9f9f9;


  text-align: center;
  position: relative;
}

.section-title {
  font-size: 2rem;
  color: #333;
  margin-bottom: 40px;
  font-weight: bold;
}

/* Carousel Wrapper */
.carousel {
  display: flex;
  overflow: hidden;
  width: 100%;
  max-width: 800px;
  margin: 0 auto;
  position: relative;
}

/* Testimonial Card */
.testimonial {
  flex: 0 0 100%;
  transition: transform 0.5s ease-in-out;
}

.testimonial-content {
  padding: 20px;
  background: white;
  border-radius: 10px;
  box-shadow: 0 4px 12px rgba(0, 0, 0, 0.1);
}

.company-logo {
  width: 100px;
  height: auto;
  margin-bottom: 15px;
}

.review {
  font-size: 1rem;
  color: #555;
  margin-bottom: 20px;
  line-height: 1.6;
}

.client-name {
  font-size: 1.2rem;
  font-weight: bold;
  color: #333;
}

.company {
  font-size: 0.9rem;
  color: #777;
  margin-top: 5px;
}

/* Carousel Controls */
.carousel-controls {
  position: absolute;
  top: 50%;
  left: 0;
  right: 0;
  display: flex;
  justify-content: space-between;
  transform: translateY(-50%);
}

.prev-btn,
.next-btn {
  background: #ff6b6b;
  color: white;
  border: none;
  border-radius: 50%;
  width: 40px;
  height: 40px;
  display: flex;
  align-items: center;
  justify-content: center;
  cursor: pointer;
  transition: background 0.3s;
}

.prev-btn:hover,
.next-btn:hover {
  background: #ff5252;
}

/* Dots Navigation */
.carousel-dots {
  margin-top: 20px;
}

.carousel-dots span {
  display: inline-block;
  width: 10px;
  height: 10px;
  background-color: #ddd;
  border-radius: 50%;
  margin: 0 5px;
  cursor: pointer;
  transition: background-color 0.3s;
}

.active-dot {
  background-color: #ff6b6b;
}

/* Responsive Design */
@media (max-width: 768px) {
  .testimonial-content {
    padding: 15px;
  }

  .company-logo {
    width: 80px;
  }
}
</style>
