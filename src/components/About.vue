<template>
  <section id="about" class="py-6 about-section">
    <!-- Background shape -->
    <div class="about-shape-circle"></div>

    <div class="container">
      <div class="row align-items-center">
        <div class="col-lg-6 mb-5 mb-lg-0 text-center position-relative">
          <div class="about-image-wrapper">
            <img src="../assets/about-light.png" alt="Collaborative workspace" class="about-illustration" />
            <!-- Floating active user badge -->
            <div class="floating-badge-about bg-white shadow-sm p-3 d-flex align-items-center gap-3">
              <div class="badge-icon-box">
                <i class="bi bi-people-fill"></i>
              </div>
              <div class="text-start">
                <h5 class="fw-bold mb-0 text-dark">1.8m</h5>
                <p class="small text-muted mb-0">Total Active Users</p>
              </div>
            </div>
          </div>
        </div>
        <div class="col-lg-6 ps-lg-5 text-center text-lg-start">
          <div class="tp-section-tag mb-2">Know About Vortex</div>
          <h2 class="tp-section-title display-6 mb-4">
            We Provide the Best Insurance Policy
          </h2>
          <p class="text-muted mb-4 fs-6 leading-relaxed">
            Platform asuransi digital kami dirancang khusus menggunakan teknologi enkripsi tercanggih untuk memastikan kenyamanan dan keamanan perlindungan finansial Anda dan keluarga tercinta.
          </p>
          <div class="about-features-container mb-4">
            <div class="about-feature-item d-flex align-items-start gap-3 mb-4">
              <div class="about-feature-icon">
                <i class="bi bi-cash-stack"></i>
              </div>
              <div>
                <h5 class="fw-bold text-dark mb-1">Moneyback Guarantee</h5>
                <p class="text-muted small mb-0">Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu nulla pariatur.</p>
              </div>
            </div>
            <div class="about-feature-item d-flex align-items-start gap-3">
              <div class="about-feature-icon">
                <i class="bi bi-headset"></i>
              </div>
              <div>
                <h5 class="fw-bold text-dark mb-1">Technical Support</h5>
                <p class="text-muted small mb-0">Tim bantuan ahli kami siap sedia 24/7 untuk melayani pengajuan klaim darurat Anda.</p>
              </div>
            </div>
          </div>
          <div class="about-actions mt-4 pt-2">
            <a href="#contact" class="tp-btn tp-btn-green py-3 px-5">
              Let's Get Started
            </a>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<style scoped>
.about-section {
  background-color: var(--bg-primary);
  padding: 100px 0;
  position: relative;
  overflow: hidden;
}

.about-shape-circle {
  position: absolute;
  top: 10%;
  left: -5%;
  width: 300px;
  height: 300px;
  background: radial-gradient(circle, rgba(0, 185, 107, 0.04) 0%, rgba(255, 255, 255, 0) 70%);
  pointer-events: none;
}

.about-image-wrapper {
  position: relative;
  max-width: 460px;
  margin: 0 auto;
  padding: 10px;
}

.about-illustration {
  width: 100%;
  height: auto;
  border-radius: 16px;
  box-shadow: var(--shadow-md);
  transition: transform 0.4s ease;
}

.about-illustration:hover {
  transform: scale(1.01) translateY(-3px);
}

/* Floating Active User Badge */
.floating-badge-about {
  position: absolute;
  bottom: 25px;
  right: -15px;
  border-radius: 12px;
  border: 1px solid rgba(15, 23, 42, 0.05);
  z-index: 3;
  min-width: 180px;
  animation: float-badge 4s ease-in-out infinite;
}

.badge-icon-box {
  width: 40px;
  height: 40px;
  border-radius: 50%;
  background-color: #e6f8f0;
  color: var(--accent-green);
  display: flex;
  align-items: center;
  justify-content: center;
  font-size: 18px;
}

.about-feature-icon {
  width: 48px;
  height: 48px;
  background-color: #e6f8f0;
  color: var(--accent-green);
  border-radius: 50%;
  display: flex;
  align-items: center;
  justify-content: center;
  font-size: 22px;
  flex-shrink: 0;
}

@keyframes float-badge {
  0%, 100% {
    transform: translateY(0);
  }
  50% {
    transform: translateY(-8px);
  }
}

@media (max-width: 991px) {
  .about-section {
    padding: 60px 0;
  }
  .floating-badge-about {
    right: 20px;
    bottom: -10px;
  }
}
</style>
