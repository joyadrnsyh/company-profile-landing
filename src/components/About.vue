<template>
  <section id="about" class="py-6 about-section">
    <!-- Glow Orb -->
    <div class="glow-orb glow-orb-about"></div>

    <div class="container">
      <div class="row align-items-center">
        <div class="col-lg-6 mb-5 mb-lg-0 text-center position-relative">
          <div class="about-image-wrapper">
            <div class="about-image-glow"></div>
            <img src="../assets/about-illustration.png" alt="Collaborative Innovation" class="about-illustration" />
          </div>
        </div>
        <div class="col-lg-6 ps-lg-5 text-center text-lg-start">
          <div class="section-tag mb-3">SIAPA KAMI</div>
          <h2 class="display-6 fw-extrabold mb-4">
            Membangun Masa Depan Dengan <span class="text-gradient">Inovasi</span>
          </h2>
          <p class="fs-6 text-muted mb-4 leading-relaxed">
            Kami adalah perusahaan teknologi yang berdedikasi untuk memberikan solusi digital terbaik bagi pertumbuhan bisnis Anda. Dengan pengalaman lebih dari 10 tahun di industri, kami menggabungkan keahlian mendalam, proses yang andal, dan teknologi canggih untuk membantu Anda memenangkan persaingan pasar.
          </p>
          <div class="row g-3">
            <div class="col-sm-6">
              <div class="feature-card glass-card d-flex align-items-start gap-3 p-3">
                <div class="feature-icon">
                  <i class="bi bi-patch-check-fill"></i>
                </div>
                <div>
                  <h6 class="fw-bold mb-1 text-white">Profesional</h6>
                  <p class="text-muted small mb-0">Tim ahli bersertifikat</p>
                </div>
              </div>
            </div>
            <div class="col-sm-6">
              <div class="feature-card glass-card d-flex align-items-start gap-3 p-3">
                <div class="feature-icon">
                  <i class="bi bi-shield-fill-check"></i>
                </div>
                <div>
                  <h6 class="fw-bold mb-1 text-white">Terpercaya</h6>
                  <p class="text-muted small mb-0">Keamanan data terjamin</p>
                </div>
              </div>
            </div>
            <div class="col-sm-6">
              <div class="feature-card glass-card d-flex align-items-start gap-3 p-3">
                <div class="feature-icon">
                  <i class="bi bi-lightbulb-fill"></i>
                </div>
                <div>
                  <h6 class="fw-bold mb-1 text-white">Inovatif</h6>
                  <p class="text-muted small mb-0">Solusi berbasis AI & IoT</p>
                </div>
              </div>
            </div>
            <div class="col-sm-6">
              <div class="feature-card glass-card d-flex align-items-start gap-3 p-3">
                <div class="feature-icon">
                  <i class="bi bi-headset"></i>
                </div>
                <div>
                  <h6 class="fw-bold mb-1 text-white">Dukungan 24/7</h6>
                  <p class="text-muted small mb-0">Respon cepat kapan saja</p>
                </div>
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<style scoped>
.about-section {
  background-color: #080f21;
  padding: 100px 0;
  position: relative;
  overflow: hidden;
}

.glow-orb-about {
  position: absolute;
  top: 30%;
  left: -10%;
  width: 400px;
  height: 400px;
  background: radial-gradient(circle, rgba(99, 102, 241, 0.1) 0%, rgba(0, 0, 0, 0) 70%);
  filter: blur(60px);
  pointer-events: none;
}

.section-tag {
  color: #06b6d4;
  font-size: 13px;
  font-weight: 700;
  letter-spacing: 2px;
}

.fw-extrabold {
  font-weight: 800;
  color: white;
}

.about-image-wrapper {
  position: relative;
  max-width: 480px;
  margin: 0 auto;
  padding: 15px;
}

.about-image-glow {
  position: absolute;
  top: 50%;
  left: 50%;
  transform: translate(-50%, -50%);
  width: 90%;
  height: 90%;
  background: radial-gradient(circle, rgba(6, 182, 212, 0.2) 0%, rgba(0, 0, 0, 0) 70%);
  filter: blur(40px);
  z-index: 1;
}

.about-illustration {
  width: 100%;
  height: auto;
  border-radius: 20px;
  position: relative;
  z-index: 2;
  box-shadow: 0 15px 30px rgba(0, 0, 0, 0.35);
  transition: transform 0.5s ease;
}

.about-illustration:hover {
  transform: scale(1.02) translateY(-5px);
}

.feature-card {
  border: 1px solid rgba(255, 255, 255, 0.05);
  background: rgba(16, 23, 41, 0.5);
  border-radius: 14px !important;
  text-align: left;
  transition: all 0.3s ease;
}

.feature-card:hover {
  transform: translateY(-3px);
  border-color: rgba(6, 182, 212, 0.3);
  background: rgba(16, 23, 41, 0.8);
  box-shadow: 0 8px 25px rgba(6, 182, 212, 0.1);
}

.feature-icon {
  width: 42px;
  height: 42px;
  background: rgba(6, 182, 212, 0.1);
  border: 1px solid rgba(6, 182, 212, 0.2);
  border-radius: 10px;
  display: flex;
  align-items: center;
  justify-content: center;
  color: #06b6d4;
  font-size: 20px;
  flex-shrink: 0;
  transition: all 0.3s ease;
}

.feature-card:hover .feature-icon {
  background: linear-gradient(135deg, #06b6d4 0%, #6366f1 100%);
  color: white;
  box-shadow: 0 0 10px rgba(6, 182, 212, 0.4);
  border-color: transparent;
}

@media (max-width: 991px) {
  .about-section {
    padding: 60px 0;
  }
}
</style>
