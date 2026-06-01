<template>
  <section id="home" class="hero-section">
    <div class="container d-flex align-items-center justify-content-center h-100">
      <div class="row w-100 align-items-center">
        <div class="col-lg-6 text-center text-lg-start mb-4 mb-lg-0">
          <h1 class="display-4 fw-bold mb-3 hero-title">
            Solusi Bisnis Terpercaya
          </h1>
          <p class="lead mb-4 text-muted">
            Kami menyediakan layanan profesional untuk mengembangkan bisnis Anda ke level berikutnya dengan teknologi terkini dan tim berpengalaman.
          </p>
          <div class="gap-3 d-flex flex-column flex-sm-row justify-content-center justify-content-lg-start">
            <button class="btn btn-primary btn-lg px-5">
              <i class="bi bi-play-fill me-2"></i> Mulai Sekarang
            </button>
            <button class="btn btn-outline-primary btn-lg px-5">
              <i class="bi bi-play-circle me-2"></i> Pelajari Lebih Lanjut
            </button>
          </div>
        </div>
        <div class="col-lg-6 text-center">
          <div class="hero-image-placeholder">
            <i class="bi bi-rocket"></i>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<style scoped>
.hero-section {
  background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
  min-height: 600px;
  color: white;
  display: flex;
  align-items: center;
  overflow: hidden;
  position: relative;
}

.hero-section::before {
  content: '';
  position: absolute;
  top: -50%;
  right: -50%;
  width: 500px;
  height: 500px;
  background: rgba(255, 255, 255, 0.1);
  border-radius: 50%;
  animation: float 6s ease-in-out infinite;
}

.hero-section::after {
  content: '';
  position: absolute;
  bottom: -30%;
  left: -30%;
  width: 400px;
  height: 400px;
  background: rgba(255, 255, 255, 0.05);
  border-radius: 50%;
  animation: float 8s ease-in-out infinite reverse;
}

.hero-title {
  font-size: 3.5rem;
  font-weight: 700;
  line-height: 1.2;
  text-shadow: 2px 2px 4px rgba(0, 0, 0, 0.1);
}

.hero-image-placeholder {
  width: 300px;
  height: 300px;
  margin: 0 auto;
  background: rgba(255, 255, 255, 0.1);
  border-radius: 20px;
  display: flex;
  align-items: center;
  justify-content: center;
  font-size: 120px;
  animation: float 4s ease-in-out infinite;
  border: 2px solid rgba(255, 255, 255, 0.2);
}

.btn-primary {
  background-color: #fff;
  color: #667eea;
  border: none;
  font-weight: 600;
  transition: 0.3s;
}

.btn-primary:hover {
  background-color: #f0f0f0;
  transform: translateY(-3px);
  box-shadow: 0 10px 20px rgba(0, 0, 0, 0.2);
}

.btn-outline-primary {
  color: white;
  border-color: white;
  font-weight: 600;
  transition: 0.3s;
}

.btn-outline-primary:hover {
  background-color: white;
  color: #667eea;
  transform: translateY(-3px);
  box-shadow: 0 10px 20px rgba(0, 0, 0, 0.2);
}

@keyframes float {
  0%,
  100% {
    transform: translateY(0px);
  }
  50% {
    transform: translateY(-20px);
  }
}

@media (max-width: 768px) {
  .hero-section {
    min-height: 400px;
    padding: 40px 0;
  }

  .hero-title {
    font-size: 2rem;
  }

  .hero-image-placeholder {
    width: 200px;
    height: 200px;
    font-size: 80px;
  }
}
</style>
