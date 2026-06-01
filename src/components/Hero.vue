<template>
  <section id="home" class="hero-section">
    <!-- Decorative background elements -->
    <div class="shape-circle shape-circle-1 animate-up-down"></div>
    <div class="shape-circle shape-circle-2"></div>

    <div class="container hero-container">
      <div class="row align-items-center pt-5 pt-lg-0">
        <div class="col-lg-7 text-center text-lg-start mb-5 mb-lg-0 hero-left">
          <div class="badge-wrapper mb-3">
            <span class="tp-slider-title-pre">
              Digital Insurance Platform
            </span>
          </div>
          <h1 class="hero-title mb-4">
            Launch Your Own Insurance Website With <span class="text-green">Vortex</span>.
          </h1>
          <p class="hero-desc mb-5">
            Platform asuransi digital terpercaya untuk mengamankan aset, bisnis, dan keluarga Anda. Didukung oleh teknologi enkripsi terbaru dan pelayanan cepat.
          </p>
          <div class="hero-actions d-flex flex-column flex-sm-row align-items-center justify-content-center justify-content-lg-start gap-4">
            <a href="#contact" class="tp-btn tp-btn-green py-3 px-5 fs-6">
              Let's Get Started
            </a>
            <div class="tp-slider-video-btn d-flex align-items-center gap-3">
              <a class="tp-video-play" href="https://www.youtube.com/watch?v=go7QYaQR494" target="_blank">
                <i class="bi bi-play-fill"></i>
              </a>
              <span class="tp-slider-work fw-bold">How It Works</span>
            </div>
          </div>
        </div>
        <div class="col-lg-5 text-center hero-right position-relative">
          <div class="hero-image-wrapper">
            <img src="../assets/hero-light.png" alt="Insurai Advisor" class="hero-illustration" />
            <!-- Decorative floating badges -->
            <div class="floating-benefit glass-badge shadow-sm py-2 px-3 animate-up-down">
              <i class="bi bi-shield-fill-check text-green me-2"></i>
              <span class="fw-bold text-dark">100% Secured Policy</span>
            </div>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<style scoped>
.hero-section {
  position: relative;
  min-height: 85vh;
  display: flex;
  align-items: center;
  padding: 100px 0;
  background-color: var(--bg-secondary);
  overflow: hidden;
}

.hero-container {
  position: relative;
  z-index: 2;
}

/* Decorative background circles */
.shape-circle {
  position: absolute;
  border-radius: 50%;
  pointer-events: none;
}

.shape-circle-1 {
  top: 15%;
  right: 45%;
  width: 40px;
  height: 40px;
  background-color: rgba(0, 185, 107, 0.15);
}

.shape-circle-2 {
  bottom: 10%;
  left: 5%;
  width: 250px;
  height: 250px;
  background: radial-gradient(circle, rgba(0, 185, 107, 0.05) 0%, rgba(255, 255, 255, 0) 70%);
}

.tp-slider-title-pre {
  background-color: #e6f8f0;
  color: var(--accent-green);
  font-size: 13.5px;
  font-weight: 700;
  letter-spacing: 1.5px;
  text-transform: uppercase;
  padding: 8px 18px;
  border-radius: 30px;
  display: inline-block;
}

.hero-title {
  font-size: 3.5rem;
  font-weight: 800;
  line-height: 1.2;
  color: var(--accent-navy);
  letter-spacing: -1px;
}

.text-green {
  color: var(--accent-green);
}

.hero-desc {
  font-size: 1.15rem;
  color: var(--text-muted);
  max-width: 580px;
  line-height: 1.7;
}

/* Image Illustration wrapper */
.hero-image-wrapper {
  position: relative;
  max-width: 450px;
  margin: 0 auto;
  z-index: 2;
}

.hero-illustration {
  width: 100%;
  height: auto;
  border-radius: 20px;
  filter: drop-shadow(0 15px 30px rgba(15, 23, 42, 0.08));
}

/* Video play button matching Insurai */
.tp-video-play {
  width: 52px;
  height: 52px;
  background-color: #ffffff;
  color: var(--accent-green);
  border-radius: 50%;
  display: flex;
  align-items: center;
  justify-content: center;
  font-size: 22px;
  box-shadow: 0 4px 15px rgba(0, 0, 0, 0.08);
  text-decoration: none;
  transition: all 0.3s ease;
  position: relative;
}

.tp-video-play:hover {
  background-color: var(--accent-green);
  color: white;
  transform: scale(1.08);
}

.tp-slider-work {
  color: var(--accent-navy);
  font-size: 15px;
  cursor: pointer;
  transition: color 0.2s ease;
}

.tp-slider-work:hover {
  color: var(--accent-green);
}

/* Floating badge */
.glass-badge {
  background: rgba(255, 255, 255, 0.9);
  backdrop-filter: blur(8px);
  border: 1px solid rgba(15, 23, 42, 0.06);
  border-radius: 12px;
}

.floating-benefit {
  position: absolute;
  bottom: 30px;
  left: -20px;
  box-shadow: 0 8px 24px rgba(15, 23, 42, 0.08);
  z-index: 3;
}

.text-green {
  color: var(--accent-green) !important;
}

@media (max-width: 991px) {
  .hero-section {
    padding: 60px 0;
  }
  .hero-title {
    font-size: 2.5rem;
  }
  .hero-desc {
    font-size: 1rem;
    margin-bottom: 30px;
  }
  .floating-benefit {
    left: 20px;
    bottom: 20px;
  }
}
</style>
