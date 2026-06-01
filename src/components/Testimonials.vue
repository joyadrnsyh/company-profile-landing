<template>
  <section id="testimonials" class="py-6 testimonials-section">
    <div class="container">
      <div class="row align-items-end mb-5">
        <div class="col-lg-8 text-center text-lg-start">
          <div class="tp-section-tag text-green mb-2">Clients Feedback</div>
          <h2 class="tp-section-title text-white display-6 mb-0">What Our Client Say<br />About Our Vortex Agency</h2>
        </div>
        <div class="col-lg-4 text-center text-lg-end mt-4 mt-lg-0">
          <a href="#contact" class="tp-btn tp-btn-green">View all Reviews</a>
        </div>
      </div>

      <div class="row g-4">
        <div class="col-md-6 col-lg-4" v-for="testimonial in testimonials" :key="testimonial.id">
          <div class="testimonial-card tp-card position-relative overflow-hidden">
            <!-- Decorative Quotation mark background -->
            <div class="quote-bg-icon">
              <i class="bi bi-quote"></i>
            </div>
            
            <div class="stars mb-3">
              <i class="bi bi-star-fill" v-for="i in 5" :key="i"></i>
            </div>
            
            <p class="testimonial-text mb-4 text-muted">{{ testimonial.text }}</p>
            
            <div class="d-flex align-items-center gap-3 profile-footer">
              <div class="client-avatar-frame">
                <i class="bi bi-person-fill"></i>
              </div>
              <div>
                <h6 class="fw-bold mb-0 text-dark">{{ testimonial.name }}</h6>
                <span class="member-role small">{{ testimonial.company }}</span>
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<script setup lang="ts">
const testimonials = [
  {
    id: 1,
    text: 'System is a term used to refer to an organized collection and to symbols and processes that may be used to operate on such symbols. Perspiciatis omnis natus.',
    name: 'Raihan',
    company: 'Developer'
  },
  {
    id: 2,
    text: 'Platform asuransi digital Vortex sangat memudahkan kami untuk melakukan registrasi dan mengklaim proteksi kendaraan kami. Prosesnya cepat dan transparan.',
    name: 'Belal Mahmud',
    company: 'Designer'
  },
  {
    id: 3,
    text: 'Customer support yang luar biasa, selalu menjawab pertanyaan kami dengan cepat dan profesional. Layanan asuransi kesehatan yang sangat direkomendasikan.',
    name: 'Mahima Minu',
    company: 'Co Founder'
  }
];
</script>

<style scoped>
.testimonials-section {
  background-color: var(--bg-dark-divider);
  padding: 100px 0;
  position: relative;
  overflow: hidden;
}

.testimonial-card {
  background: #ffffff !important;
  border: none !important;
  height: 100%;
  display: flex;
  flex-direction: column;
  justify-content: space-between;
}

.quote-bg-icon {
  position: absolute;
  top: -10px;
  right: 15px;
  font-size: 110px;
  color: rgba(15, 23, 42, 0.03);
  pointer-events: none;
  line-height: 1;
}

.stars {
  color: #fbbf24;
  font-size: 14px;
  letter-spacing: 2px;
}

.testimonial-text {
  font-size: 14.5px;
  line-height: 1.6;
  font-style: italic;
  position: relative;
  z-index: 2;
  flex-grow: 1;
}

.profile-footer {
  position: relative;
  z-index: 2;
  margin-top: 15px;
}

.client-avatar-frame {
  width: 42px;
  height: 42px;
  background-color: #e6f8f0;
  color: var(--accent-green);
  border-radius: 50%;
  display: flex;
  align-items: center;
  justify-content: center;
  font-size: 20px;
}

.member-role {
  color: var(--accent-green);
  font-weight: 600;
}

.text-green {
  color: var(--accent-green) !important;
}

@media (max-width: 991px) {
  .testimonials-section {
    padding: 60px 0;
  }
}
</style>
