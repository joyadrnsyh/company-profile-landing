<template>
  <nav class="navbar navbar-expand-lg sticky-top custom-navbar">
    <div class="container">
      <a class="navbar-brand d-flex align-items-center gap-2" href="#home">
        <div class="logo-box">
          <i class="bi bi-cpu-fill"></i>
        </div>
        <span class="brand-text">VORTEX</span>
      </a>
      <button
        class="navbar-toggler"
        type="button"
        data-bs-toggle="collapse"
        data-bs-target="#navbarNav"
        aria-controls="navbarNav"
        aria-expanded="false"
        aria-label="Toggle navigation"
      >
        <span class="navbar-toggler-icon-custom">
          <span></span>
          <span></span>
          <span></span>
        </span>
      </button>
      <div class="collapse navbar-collapse" id="navbarNav">
        <ul class="navbar-nav ms-auto align-items-center gap-lg-3 gap-2 py-3 py-lg-0">
          <li class="nav-item">
            <a class="nav-link active" href="#home">Home</a>
          </li>
          <li class="nav-item">
            <a class="nav-link" href="#about">Tentang Kami</a>
          </li>
          <li class="nav-item">
            <a class="nav-link" href="#services">Layanan</a>
          </li>
          <li class="nav-item">
            <a class="nav-link" href="#team">Tim</a>
          </li>
          <li class="nav-item">
            <a class="nav-link" href="#testimonials">Testimoni</a>
          </li>
          <li class="nav-item">
            <a class="nav-link" href="#contact">Hubungi Kami</a>
          </li>
          <li class="nav-item ms-lg-2">
            <a href="#contact" class="btn btn-glow-primary btn-sm px-4 py-2">Daftar</a>
          </li>
        </ul>
      </div>
    </div>
  </nav>
</template>

<style scoped>
.custom-navbar {
  background: rgba(4, 7, 17, 0.75) !important;
  backdrop-filter: blur(16px);
  -webkit-backdrop-filter: blur(16px);
  border-bottom: 1px solid rgba(255, 255, 255, 0.08);
  padding: 15px 0;
  transition: all 0.3s ease;
  z-index: 1000;
}

.logo-box {
  width: 38px;
  height: 38px;
  background: linear-gradient(135deg, #06b6d4 0%, #6366f1 100%);
  border-radius: 10px;
  display: flex;
  align-items: center;
  justify-content: center;
  color: white;
  font-size: 20px;
  box-shadow: 0 0 15px rgba(6, 182, 212, 0.4);
}

.brand-text {
  font-size: 1.4rem;
  font-weight: 800;
  letter-spacing: 1.5px;
  background: linear-gradient(135deg, #ffffff 0%, #cbd5e1 50%, #94a3b8 100%);
  -webkit-background-clip: text;
  -webkit-text-fill-color: transparent;
  background-clip: text;
}

.nav-link {
  color: #94a3b8;
  font-weight: 500;
  font-size: 15px;
  padding: 8px 16px !important;
  transition: all 0.3s ease;
  position: relative;
}

.nav-link:hover,
.nav-link.active {
  color: #06b6d4;
}

/* Sliding active link indicator line */
.nav-link::after {
  content: '';
  position: absolute;
  bottom: 0;
  left: 16px;
  right: 16px;
  height: 2px;
  background: linear-gradient(90deg, #06b6d4, #6366f1);
  transform: scaleX(0);
  transition: transform 0.3s ease;
  transform-origin: bottom left;
}

.nav-link.active::after,
.nav-link:hover::after {
  transform: scaleX(1);
}

/* Mobile Toggler Custom Styling */
.navbar-toggler {
  border: none;
  padding: 0;
  outline: none;
}

.navbar-toggler:focus {
  box-shadow: none;
}

.navbar-toggler-icon-custom {
  display: flex;
  flex-direction: column;
  justify-content: space-between;
  width: 24px;
  height: 18px;
}

.navbar-toggler-icon-custom span {
  display: block;
  height: 2.5px;
  width: 100%;
  background-color: #cbd5e1;
  border-radius: 2px;
  transition: all 0.3s ease;
}

.navbar-toggler[aria-expanded="true"] .navbar-toggler-icon-custom span:nth-child(1) {
  transform: translateY(8px) rotate(45deg);
}

.navbar-toggler[aria-expanded="true"] .navbar-toggler-icon-custom span:nth-child(2) {
  opacity: 0;
}

.navbar-toggler[aria-expanded="true"] .navbar-toggler-icon-custom span:nth-child(3) {
  transform: translateY(-8px) rotate(-45deg);
}

@media (max-width: 991px) {
  .navbar-nav {
    text-align: center;
  }
  .nav-link::after {
    display: none;
  }
}
</style>
