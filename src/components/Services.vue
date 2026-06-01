<template>
  <section id="services" class="py-6 services-section">
    <!-- Background shape -->
    <div class="services-shape-circle"></div>

    <div class="container">
      <div class="text-center mb-5">
        <div class="tp-section-tag mb-2">Our Services</div>
        <h2 class="tp-section-title display-6">We're Giving all the <br />Insurance Services to You</h2>
      </div>

      <div class="row g-4">
        <div class="col-md-6 col-lg-4" v-for="service in services" :key="service.id">
          <div class="service-card tp-card d-flex flex-column align-items-center text-center">
            <div class="tp-icon-circle mb-4">
              <i :class="service.icon"></i>
            </div>
            <h4 class="fw-bold mb-3 text-dark">{{ service.title }}</h4>
            <p class="text-muted mb-4 small-text">{{ service.description }}</p>
            <a href="#contact" class="service-link fw-bold text-decoration-none d-inline-flex align-items-center">
              Read More <i class="bi bi-chevron-right ms-2 arrow-icon"></i>
            </a>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<script setup lang="ts">
const services = [
  {
    id: 1,
    icon: 'bi bi-car-front-fill',
    title: 'Car Insurance',
    description: 'A car insurance policy will cover the cost of repairing or replacing your vehicle after an accident.'
  },
  {
    id: 2,
    icon: 'bi bi-house-heart-fill',
    title: 'Home Insurance',
    description: 'Protect your home structure and personal belongings from fire, theft, and natural disasters.'
  },
  {
    id: 3,
    icon: 'bi bi-shield-heart',
    title: 'Life Insurance',
    description: 'Secure your family financial future in case of unexpected events with our trusted life policies.'
  },
  {
    id: 4,
    icon: 'bi bi-heart-pulse-fill',
    title: 'Health Insurance',
    description: 'Comprehensive medical coverage options designed to help you and your family manage health costs.'
  },
  {
    id: 5,
    icon: 'bi bi-briefcase-fill',
    title: 'Business Insurance',
    description: 'Shield your business assets, employees, and operations from liabilities and business disruptions.'
  },
  {
    id: 6,
    icon: 'bi bi-airplane-fill',
    title: 'Travel Insurance',
    description: 'Enjoy your trips worry-free with coverage for trip cancellations, medical emergencies, and lost baggage.'
  }
];
</script>

<style scoped>
.services-section {
  background-color: var(--bg-secondary);
  padding: 100px 0;
  position: relative;
  overflow: hidden;
}

.services-shape-circle {
  position: absolute;
  bottom: -5%;
  right: -5%;
  width: 300px;
  height: 300px;
  background: radial-gradient(circle, rgba(0, 185, 107, 0.04) 0%, rgba(255, 255, 255, 0) 70%);
  pointer-events: none;
}

.tp-card {
  background: #ffffff;
  padding: 40px 30px;
  border-radius: 16px;
  box-shadow: 0 10px 30px rgba(0, 0, 0, 0.05);
  transition: transform 0.3s ease;
}

.tp-icon-circle {
  width: 70px;
  height: 70px;
  background: rgba(0, 185, 107, 0.1);
  color: var(--accent-green);
  border-radius: 50%;
  display: flex;
  align-items: center;
  justify-content: center;
  font-size: 28px;
}

.service-card {
  height: 100%;
}

.small-text {
  font-size: 14.5px;
  line-height: 1.6;
  flex-grow: 1;
}

.service-link {
  color: var(--text-primary);
  font-size: 14px;
  transition: all 0.2s ease;
}

.arrow-icon {
  font-size: 12px;
  transition: transform 0.2s ease;
}

.service-card:hover .service-link {
  color: var(--accent-green);
}

.service-card:hover .arrow-icon {
  transform: translateX(4px);
}

@media (max-width: 991px) {
  .services-section {
    padding: 60px 0;
  }
}
</style>
