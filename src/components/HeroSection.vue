<template>
  <section class="hero-section">
    <div class="hero-content">
      <!-- Headline with Vue transition effect -->
      <transition name="fade-up">
        <h1 v-if="isVisible" class="hero-title">{{ title }}</h1>
      </transition>

      <!-- Subheading with delayed transition -->
      <transition name="fade-up">
        <p v-if="isVisible" class="hero-subtitle">{{ subtitle }}</p>
      </transition>

      <!-- Call-to-Action Buttons -->
      <div class="cta-buttons">
        <transition name="fade-up">
          <button v-if="isVisible" class="cta-btn primary" @click="handleConsultationClick">
            {{ ctaPrimary }}
          </button>
        </transition>
        <transition name="fade-up">
          <button v-if="isVisible" class="cta-btn secondary" @click="handleLearnMoreClick">
            {{ ctaSecondary }}
          </button>
        </transition>
      </div>
    </div>

    <!-- Background Interactive Animation -->
    <div class="background-animation">
      <canvas ref="networkCanvas"></canvas>
    </div>
  </section>
</template>

<script>
import { ref, onMounted } from "vue";

export default {
  name: "HeroSection",
  data() {
    return {
      title: "Empowering Your Business with Cutting-Edge IT Solutions",
      subtitle: "Tailored IT services for security, growth, and innovation",
      ctaPrimary: "Get a Free Consultation",
      ctaSecondary: "Learn More",
      isVisible: false, // Controls visibility for transitions
    };
  },
  mounted() {
    // Display the content after the component is mounted for transitions
    setTimeout(() => {
      this.isVisible = true;
    }, 500);

    // Initialize background animation after mounting
    this.animateNetwork();
  },
  methods: {
    handleConsultationClick() {
      alert("Redirect to Consultation Page");
    },
    handleLearnMoreClick() {
      alert("Redirect to Learn More Page");
    },
    animateNetwork() {
      const canvas = this.$refs.networkCanvas;
      const ctx = canvas.getContext("2d");
      let width, height;

      const resizeCanvas = () => {
        width = canvas.width = window.innerWidth;
        height = canvas.height = window.innerHeight;
      };

      const draw = () => {
        ctx.clearRect(0, 0, width, height);
        // Animation logic here
        requestAnimationFrame(draw);
      };

      resizeCanvas();
      window.addEventListener("resize", resizeCanvas);
      requestAnimationFrame(draw);
    },
  },
};
</script>

<style scoped>
/* Hero Section Styling */
.hero-section {
  position: relative;
  display: flex;
  align-items: center;
  justify-content: center;
  height: 100vh;
  padding: 0 30px;
  background:linear-gradient(to right, #54686e, #ff5252);
  overflow: hidden;
  color: white;
  text-align: center;
  /* z-index: 1; */
}

/* Headline & Subheading */
.hero-title {
  font-size: 3rem;
  font-weight: bold;
  margin-bottom: 20px;
  line-height: 1.2;
}

.hero-subtitle {
  font-size: 1.5rem;
  margin-bottom: 40px;
  color: #d1d1d1;
}

/* CTA Buttons */
.cta-buttons {
  display: flex;
  gap: 20px;
  justify-content: center;
}

.cta-btn {
  padding: 15px 30px;
  border: none;
  cursor: pointer;
  font-size: 1.2rem;
  border-radius: 5px;
  transition: background-color 0.3s ease;
}

.cta-btn.primary {
  background-color: #ff6b6b;
  color: white;
}

.cta-btn.secondary {
  background-color: transparent;
  border: 2px solid #ff6b6b;
  color: #ff6b6b;
}

.cta-btn.primary:hover {
  background-color: #ff5252;
}

.cta-btn.secondary:hover {
  background-color: #ff6b6b;
  color: white;
}

/* Background Animation */
.background-animation {
  position: absolute;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  overflow: hidden;
  z-index: -1;
}

canvas {
  width: 100%;
  height: 100%;
  display: block;
}

/* Transition Effects */
.fade-up-enter-active, .fade-up-leave-active {
  transition: opacity 0.6s ease, transform 0.6s ease;
}

.fade-up-enter, .fade-up-leave-to {
  opacity: 0;
  transform: translateY(30px);
}

@media (max-width: 768px) {
  .hero-title {
    font-size: 2.5rem;
  }

  .hero-subtitle {
    font-size: 1.2rem;
  }

  .cta-buttons {
    flex-direction: column;
    gap: 15px;
  }

  .cta-btn {
    width: 100%;
  }
}
</style>
