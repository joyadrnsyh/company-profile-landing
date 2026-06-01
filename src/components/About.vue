<template>
  <section id="about" class="py-5 bg-light">
    <div class="container">
      <div class="row align-items-center">
        <div class="col-lg-6 mb-4 mb-lg-0">
          <div class="about-image-placeholder">
            <i class="bi bi-people"></i>
          </div>
        </div>
        <div class="col-lg-6 ps-lg-5">
          <h2 class="display-5 fw-bold mb-3">Tentang Kami</h2>
          <p class="fs-5 text-muted mb-3">
            Kami adalah perusahaan yang berdedikasi untuk memberikan solusi terbaik bagi klien kami. Dengan pengalaman lebih dari 10 tahun di industri, kami telah membantu ribuan bisnis mencapai tujuan mereka.
          </p>
          <div class="row mb-4">
            <div class="col-md-6 mb-3">
              <div class="d-flex align-items-start gap-3">
                <div class="icon-box">
                  <i class="bi bi-check-circle-fill"></i>
                </div>
                <div>
                  <h5 class="fw-bold">Profesional</h5>
                  <p class="text-muted small mb-0">Tim ahli yang berpengalaman</p>
                </div>
              </div>
            </div>
            <div class="col-md-6 mb-3">
              <div class="d-flex align-items-start gap-3">
                <div class="icon-box">
                  <i class="bi bi-check-circle-fill"></i>
                </div>
                <div>
                  <h5 class="fw-bold">Terpercaya</h5>
                  <p class="text-muted small mb-0">Dipercaya ribuan klien</p>
                </div>
              </div>
            </div>
          </div>
          <div class="row">
            <div class="col-md-6 mb-3">
              <div class="d-flex align-items-start gap-3">
                <div class="icon-box">
                  <i class="bi bi-check-circle-fill"></i>
                </div>
                <div>
                  <h5 class="fw-bold">Inovatif</h5>
                  <p class="text-muted small mb-0">Teknologi terkini</p>
                </div>
              </div>
            </div>
            <div class="col-md-6 mb-3">
              <div class="d-flex align-items-start gap-3">
                <div class="icon-box">
                  <i class="bi bi-check-circle-fill"></i>
                </div>
                <div>
                  <h5 class="fw-bold">Dukungan 24/7</h5>
                  <p class="text-muted small mb-0">Siap membantu Anda</p>
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
.about-image-placeholder {
  width: 100%;
  aspect-ratio: 1;
  background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
  border-radius: 15px;
  display: flex;
  align-items: center;
  justify-content: center;
  font-size: 80px;
  color: white;
  box-shadow: 0 10px 30px rgba(0, 0, 0, 0.1);
}

.icon-box {
  width: 40px;
  height: 40px;
  background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
  border-radius: 50%;
  display: flex;
  align-items: center;
  justify-content: center;
  color: white;
  font-size: 20px;
  flex-shrink: 0;
}

h2 {
  color: #333;
}

@media (max-width: 768px) {
  .about-image-placeholder {
    font-size: 60px;
  }
}
</style>
