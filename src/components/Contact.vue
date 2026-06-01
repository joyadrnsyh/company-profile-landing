<template>
  <section id="contact" class="py-6 contact-section">
    <!-- Background shape -->
    <div class="contact-shape-circle"></div>

    <div class="container">
      <div class="text-center mb-5">
        <div class="tp-section-tag mb-2">Contact Form</div>
        <h2 class="tp-section-title display-6">Let’s Talk With Experience Advisors</h2>
      </div>

      <div class="row g-4 justify-content-center">
        <!-- Left: headphone advisory panel -->
        <div class="col-lg-4">
          <div class="advisory-box p-4 h-100 d-flex flex-column justify-content-center">
            <div class="advisory-icon-box mb-4">
              <i class="bi bi-headset"></i>
            </div>
            <h3 class="fw-bold text-dark mb-3">Let’s Talk With Experience Advisors.</h3>
            <p class="text-muted small-text mb-0">
              Platform proteksi kami dirancang untuk menjamin kenyamanan Anda. Hubungi penasihat asuransi kami untuk mendapatkan rekomendasi produk yang paling cocok.
            </p>
          </div>
        </div>

        <!-- Middle: Tabs controller -->
        <div class="col-lg-2">
          <div class="d-flex flex-row flex-lg-column justify-content-center gap-3 h-100 align-items-center py-3">
            <button
              class="tab-btn-pill"
              :class="{ active: activeTab === 'health' }"
              @click="activeTab = 'health'"
              title="Health Insurance"
            >
              <i class="bi bi-heart-pulse-fill"></i>
            </button>
            <button
              class="tab-btn-pill"
              :class="{ active: activeTab === 'home' }"
              @click="activeTab = 'home'"
              title="Home Insurance"
            >
              <i class="bi bi-house-heart-fill"></i>
            </button>
            <button
              class="tab-btn-pill"
              :class="{ active: activeTab === 'life' }"
              @click="activeTab = 'life'"
              title="Life Insurance"
            >
              <i class="bi bi-shield-heart"></i>
            </button>
            <button
              class="tab-btn-pill"
              :class="{ active: activeTab === 'vehicle' }"
              @click="activeTab = 'vehicle'"
              title="Vehicle Insurance"
            >
              <i class="bi bi-car-front-fill"></i>
            </button>
          </div>
        </div>

        <!-- Right: Tab form details -->
        <div class="col-lg-6">
          <div class="form-wrapper-light p-4 p-md-5">
            <form @submit.prevent="handleSubmit">
              <h3 class="fw-bold text-dark mb-4 capitalize-text">
                {{ activeTab }} Insurance Form
              </h3>
              
              <div class="mb-3">
                <label class="form-label text-dark fw-bold small mb-1">Full Name</label>
                <input type="text" class="form-control form-input-light" placeholder="Full name" required />
              </div>

              <div class="mb-3">
                <label class="form-label text-dark fw-bold small mb-1">Email Address</label>
                <input type="email" class="form-control form-input-light" placeholder="example@gmail.com" required />
              </div>

              <div class="mb-4">
                <label class="form-label text-dark fw-bold small mb-1">Your Message Here</label>
                <textarea class="form-control form-input-light" rows="3" placeholder="Tulis pesan atau pertanyaan Anda..." required></textarea>
              </div>

              <!-- limits of balance slider -->
              <div class="mb-4 slider-container">
                <div class="d-flex justify-content-between align-items-center mb-2">
                  <label class="form-label text-dark fw-bold small mb-0">Limits of Balance</label>
                  <span class="fw-bold text-green">${{ formattedBalance }}</span>
                </div>
                <input
                  type="range"
                  class="slider-range"
                  min="10000"
                  max="500000"
                  step="5000"
                  v-model="balanceLimit"
                />
              </div>

              <button type="submit" class="tp-btn tp-btn-green w-100 py-3 mt-2">
                Send Message
              </button>
            </form>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<script setup lang="ts">
import { ref, computed } from 'vue'

const activeTab = ref('health')
const balanceLimit = ref(50000)

const formattedBalance = computed(() => {
  return Number(balanceLimit.value).toLocaleString('en-US')
})

function handleSubmit() {
  alert(`Terima kasih! Permintaan penawaran ${activeTab.value} insurance Anda dengan limit balance $${formattedBalance.value} telah terkirim. Advisor kami akan segera menghubungi Anda.`)
}
</script>

<style scoped>
.contact-section {
  background-color: var(--bg-primary);
  padding: 100px 0;
  position: relative;
  overflow: hidden;
}

.contact-shape-circle {
  position: absolute;
  bottom: 10%;
  left: -5%;
  width: 400px;
  height: 400px;
  background: radial-gradient(circle, rgba(0, 185, 107, 0.03) 0%, rgba(255, 255, 255, 0) 70%);
  pointer-events: none;
}

.advisory-box {
  background-color: var(--bg-secondary);
  border: 1px solid var(--border-light);
  border-radius: 16px;
  text-align: center;
}

.advisory-icon-box {
  width: 60px;
  height: 60px;
  background-color: #e6f8f0;
  color: var(--accent-green);
  border-radius: 50%;
  display: flex;
  align-items: center;
  justify-content: center;
  font-size: 26px;
  margin: 0 auto;
}

/* Tabs pills matching Insurai list */
.tab-btn-pill {
  width: 54px;
  height: 54px;
  border-radius: 50%;
  border: 1px solid rgba(15, 23, 42, 0.08);
  background-color: #ffffff;
  color: var(--accent-navy);
  font-size: 20px;
  display: flex;
  align-items: center;
  justify-content: center;
  cursor: pointer;
  transition: all 0.3s cubic-bezier(0.16, 1, 0.3, 1);
  box-shadow: var(--shadow-sm);
}

.tab-btn-pill:hover,
.tab-btn-pill.active {
  background-color: var(--accent-green);
  color: #ffffff;
  border-color: var(--accent-green);
  box-shadow: 0 4px 12px rgba(0, 185, 107, 0.25);
  transform: scale(1.08);
}

.form-wrapper-light {
  background: #ffffff;
  border: 1px solid var(--border-light);
  border-radius: 16px;
  box-shadow: var(--shadow-md);
}

.capitalize-text {
  text-transform: capitalize;
}

.text-green {
  color: var(--accent-green) !important;
}

.small-text {
  font-size: 14.5px;
  line-height: 1.6;
}

@media (max-width: 991px) {
  .contact-section {
    padding: 60px 0;
  }
}
</style>
