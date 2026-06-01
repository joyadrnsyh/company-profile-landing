<template>
  <section id="home" class="hero-section">
    <!-- Glowing Orbs in Background -->
    <div class="glow-orb glow-orb-1"></div>
    <div class="glow-orb glow-orb-2"></div>

    <div class="container hero-container d-flex align-items-center">
      <div class="row w-100 align-items-center pt-5 pt-lg-0">
        <div class="col-lg-6 text-center text-lg-start mb-5 mb-lg-0 hero-left">
          <div class="badge-wrapper mb-3">
            <span class="badge-custom">
              <i class="bi bi-cpu-fill me-2 text-cyan animate-pulse"></i>
              Partner Transformasi Digital Terbaik
            </span>
          </div>
          <h1 class="hero-title mb-3">
            Solusi Bisnis Terpercaya Untuk Era <span class="text-gradient">Digital</span>
          </h1>
          <p class="hero-desc mb-4">
            Kami menyediakan layanan IT profesional kelas dunia untuk mengembangkan bisnis Anda ke level berikutnya dengan teknologi terkini, infrastruktur handal, dan tim ahli berpengalaman.
          </p>
          <div class="gap-3 d-flex flex-column flex-sm-row justify-content-center justify-content-lg-start hero-actions">
            <a href="#contact" class="btn btn-glow-primary btn-lg d-flex align-items-center justify-content-center">
              <i class="bi bi-rocket-takeoff-fill me-2"></i> Mulai Sekarang
            </a>
            <a href="#about" class="btn btn-glow-outline btn-lg d-flex align-items-center justify-content-center">
              Pelajari Lebih Lanjut <i class="bi bi-arrow-right ms-2"></i>
            </a>
          </div>
        </div>
        <div class="col-lg-6 text-center hero-right">
          <div class="hero-image-wrapper">
            <div class="image-bg-glow"></div>
            <img src="../assets/hero-illustration.png" alt="Vortex Cloud Tech" class="hero-illustration" />
            <!-- Floating Badge Overlay -->
            <div class="floating-badge glass-card py-2 px-3 d-flex align-items-center gap-2">
              <div class="avatar-group d-flex">
                <i class="bi bi-person-circle text-info"></i>
                <i class="bi bi-person-circle text-primary ms-n2"></i>
                <i class="bi bi-person-circle text-warning ms-n2"></i>
              </div>
              <div class="text-start">
                <div class="badge-title fw-bold">1,000+ Klien</div>
                <div class="badge-subtitle text-muted">Telah terbantu di seluruh dunia</div>
              </div>
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
  min-height: 80vh;
  display: flex;
  align-items: center;
  padding: 100px 0;
  background-color: #040711;
  overflow: hidden;
}

.hero-container {
  z-index: 2;
}

/* Background Glow Orbs */
.glow-orb-1 {
  position: absolute;
  top: -10%;
  right: -5%;
  width: 500px;
  height: 500px;
  background: radial-gradient(circle, rgba(6, 182, 212, 0.15) 0%, rgba(99, 102, 241, 0.03) 60%, rgba(0, 0, 0, 0) 100%);
  filter: blur(80px);
  pointer-events: none;
  animation: float-slow 15s ease-in-out infinite;
}

.glow-orb-2 {
  position: absolute;
  bottom: -10%;
  left: -5%;
  width: 400px;
  height: 400px;
  background: radial-gradient(circle, rgba(168, 85, 247, 0.12) 0%, rgba(6, 182, 212, 0.02) 60%, rgba(0, 0, 0, 0) 100%);
  filter: blur(80px);
  pointer-events: none;
  animation: float-slow 20s ease-in-out infinite reverse;
}

/* Badge wrapper */
.badge-custom {
  background: rgba(255, 255, 255, 0.04);
  border: 1px solid rgba(255, 255, 255, 0.08);
  padding: 8px 16px;
  border-radius: 50px;
  font-size: 14px;
  font-weight: 600;
  color: #38bdf8;
  display: inline-flex;
  align-items: center;
}

.text-cyan {
  color: #06b6d4;
}

.hero-title {
  font-size: 3.5rem;
  font-weight: 800;
  line-height: 1.15;
  color: white;
  letter-spacing: -1px;
}

.hero-desc {
  font-size: 1.15rem;
  color: #94a3b8;
  line-height: 1.7;
}

/* Image styling and glows */
.hero-image-wrapper {
  position: relative;
  max-width: 520px;
  margin: 0 auto;
  padding: 20px;
}

.image-bg-glow {
  position: absolute;
  top: 50%;
  left: 50%;
  transform: translate(-50%, -50%);
  width: 90%;
  height: 90%;
  background: radial-gradient(circle, rgba(99, 102, 241, 0.25) 0%, rgba(0, 0, 0, 0) 70%);
  filter: blur(40px);
  z-index: 1;
}

.hero-illustration {
  width: 100%;
  height: auto;
  border-radius: 24px;
  z-index: 2;
  position: relative;
  filter: drop-shadow(0 15px 30px rgba(0, 0, 0, 0.4));
  animation: float-hero 6s ease-in-out infinite;
}

/* Floating Badge Overlay */
.floating-badge {
  position: absolute;
  bottom: 40px;
  left: -20px;
  z-index: 3;
  box-shadow: 0 15px 35px rgba(0, 0, 0, 0.4);
  animation: float-badge 5s ease-in-out infinite;
  display: flex;
  align-items: center;
}

.avatar-group i {
  font-size: 24px;
}
.ms-n2 {
  margin-left: -8px !important;
}

.badge-title {
  font-size: 14px;
  color: white;
}
.badge-subtitle {
  font-size: 11px;
}

/* Animations */
@keyframes float-hero {
  0%, 100% {
    transform: translateY(0px) rotate(0deg);
  }
  50% {
    transform: translateY(-12px) rotate(0.5deg);
  }
}

@keyframes float-badge {
  0%, 100% {
    transform: translateY(0px);
  }
  50% {
    transform: translateY(-8px);
  }
}

@keyframes float-slow {
  0%, 100% {
    transform: translateY(0) scale(1);
  }
  50% {
    transform: translateY(-30px) scale(1.05);
  }
}

@keyframes pulse {
  0%, 100% {
    opacity: 1;
  }
  50% {
    opacity: 0.5;
  }
}
.animate-pulse {
  animation: pulse 2s cubic-bezier(0.4, 0, 0.6, 1) infinite;
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
  }
  .floating-badge {
    left: 20px;
    bottom: 20px;
  }
}
</style>
