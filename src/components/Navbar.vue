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
            <a class="nav-link" href="#about">About</a>
          </li>
          <li class="nav-item">
            <a class="nav-link" href="#services">Insurance</a>
          </li>
          <li class="nav-item">
            <a class="nav-link" href="#team">Team</a>
          </li>
          <li class="nav-item">
            <a class="nav-link" href="#testimonials">Testimonials</a>
          </li>
          <li class="nav-item">
            <a class="nav-link" href="#contact">Contact</a>
          </li>
          <li class="nav-item d-none d-xxl-block ms-lg-3">
            <div class="tp-header-tel-box d-flex align-items-center gap-2">
              <div class="tp-header-tel-icon">
                <i class="bi bi-telephone-fill"></i>
              </div>
              <div class="tp-header-tel-text text-start">
                <span class="tel-label text-muted d-block">Talk to an expert</span>
                <a href="tel:+997868765" class="tel-number fw-bold">Free +99 (786) 8765</a>
              </div>
            </div>
          </li>
          <li class="nav-item ms-lg-2">
            <a href="#contact" class="tp-btn tp-btn-green py-2 px-4">Get a Quote</a>
          </li>
        </ul>
      </div>
    </div>
  </nav>
</template>

<style scoped>
.custom-navbar {
  background: #ffffff !important;
  border-bottom: 1px solid rgba(15, 23, 42, 0.06);
  padding: 18px 0;
  transition: all 0.3s ease;
  z-index: 1000;
}

.logo-box {
  width: 36px;
  height: 36px;
  background: var(--accent-green);
  border-radius: 8px;
  display: flex;
  align-items: center;
  justify-content: center;
  color: white;
  font-size: 18px;
}

.brand-text {
  font-size: 1.35rem;
  font-weight: 800;
  letter-spacing: 1px;
  color: var(--accent-navy);
}

.nav-link {
  color: #5e6675;
  font-weight: 700;
  font-size: 15px;
  padding: 8px 12px !important;
  transition: all 0.2s ease;
}

.nav-link:hover,
.nav-link.active {
  color: var(--accent-green);
}

/* Telephone box */
.tp-header-tel-box {
  border-left: 1px solid rgba(15, 23, 42, 0.08);
  padding-left: 15px;
}

.tp-header-tel-icon {
  width: 38px;
  height: 38px;
  background-color: #e6f8f0;
  color: var(--accent-green);
  border-radius: 50%;
  display: flex;
  align-items: center;
  justify-content: center;
  font-size: 15px;
}

.tel-label {
  font-size: 11px;
  text-transform: uppercase;
  letter-spacing: 0.5px;
  margin-bottom: 2px;
}

.tel-number {
  font-size: 13.5px;
  color: var(--accent-navy);
  text-decoration: none;
  transition: color 0.2s ease;
}

.tel-number:hover {
  color: var(--accent-green);
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
  height: 16px;
}

.navbar-toggler-icon-custom span {
  display: block;
  height: 2.5px;
  width: 100%;
  background-color: var(--accent-navy);
  border-radius: 2px;
  transition: all 0.3s ease;
}

.navbar-toggler[aria-expanded="true"] .navbar-toggler-icon-custom span:nth-child(1) {
  transform: translateY(7px) rotate(45deg);
}

.navbar-toggler[aria-expanded="true"] .navbar-toggler-icon-custom span:nth-child(2) {
  opacity: 0;
}

.navbar-toggler[aria-expanded="true"] .navbar-toggler-icon-custom span:nth-child(3) {
  transform: translateY(-7px) rotate(-45deg);
}

@media (max-width: 991px) {
  .navbar-nav {
    text-align: center;
  }
  .tp-header-tel-box {
    border-left: none;
    padding-left: 0;
    justify-content: center;
    margin: 10px 0;
  }
}
</style>
