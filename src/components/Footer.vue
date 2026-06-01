<template>
  <footer class="footer">
    <div class="container py-5">
      <div class="row g-4 mb-5">
        <div class="col-lg-3 col-md-6">
          <div class="footer-brand mb-3">
            <div class="brand-logo-box d-inline-flex align-items-center gap-2 mb-3">
              <div class="logo-box-mini">
                <i class="bi bi-cpu-fill"></i>
              </div>
              <span class="brand-name">VORTEX</span>
            </div>
            <p class="small text-muted leading-relaxed">
              Platform proteksi asuransi digital terpercaya untuk mengamankan aset, keluarga, dan bisnis Anda dengan pelayanan responsif 24/7.
            </p>
          </div>
        </div>
        <div class="col-lg-2 col-md-6 offset-lg-1">
          <h6 class="fw-bold mb-3 text-white">Company</h6>
          <ul class="list-unstyled footer-links-list">
            <li><a href="#about" class="footer-link">About Us</a></li>
            <li><a href="#" class="footer-link">Blog & News</a></li>
            <li><a href="#" class="footer-link">Careers</a></li>
            <li><a href="#" class="footer-link">Claim Process</a></li>
          </ul>
        </div>
        <div class="col-lg-3 col-md-6">
          <h6 class="fw-bold mb-3 text-white">Insurance Products</h6>
          <ul class="list-unstyled footer-links-list">
            <li><a href="#services" class="footer-link">Car Insurance</a></li>
            <li><a href="#services" class="footer-link">Home Insurance</a></li>
            <li><a href="#services" class="footer-link">Life Insurance</a></li>
            <li><a href="#services" class="footer-link">Health Insurance</a></li>
          </ul>
        </div>
        <div class="col-lg-3 col-md-6">
          <h6 class="fw-bold mb-3 text-white">Berlangganan Newsletter</h6>
          <p class="small text-muted mb-3">Dapatkan artikel teknologi dan penawaran menarik langsung di inbox Anda.</p>
          <form @submit.prevent="handleSubscribe" class="newsletter-form mb-3">
            <div class="input-group">
              <input type="email" class="form-control form-input-glow" placeholder="Email Anda" required />
              <button class="btn tp-btn tp-btn-green px-3" type="submit">
                <i class="bi bi-arrow-right"></i>
              </button>
            </div>
          </form>
          <div class="social-links-row mt-3">
            <a href="#" class="social-icon fb"><i class="bi bi-facebook"></i></a>
            <a href="#" class="social-icon tw"><i class="bi bi-twitter-x"></i></a>
            <a href="#" class="social-icon li"><i class="bi bi-linkedin"></i></a>
            <a href="#" class="social-icon ig"><i class="bi bi-instagram"></i></a>
          </div>
        </div>
      </div>

      <hr class="footer-divider" />

      <div class="row align-items-center pt-2">
        <div class="col-md-6 text-center text-md-start">
          <p class="text-muted small mb-0">&copy; 2026 Vortex Solutions. All rights reserved.</p>
        </div>
        <div class="col-md-6 text-center text-md-end mt-3 mt-md-0">
          <ul class="list-inline mb-0">
            <li class="list-inline-item">
              <a href="#" class="footer-link small">Privacy Policy</a>
            </li>
            <li class="list-inline-item ms-3">
              <a href="#" class="footer-link small">Terms of Service</a>
            </li>
            <li class="list-inline-item ms-3">
              <a href="#" class="footer-link small">Cookie Policy</a>
            </li>
          </ul>
        </div>
      </div>
    </div>
  </footer>
</template>

<script setup lang="ts">
function handleSubscribe() {
  alert('Terima kasih! Email Anda telah terdaftar dalam newsletter kami.')
}
</script>

<style scoped>
.footer {
  background: #080f1e;
  color: #94a3b8;
  border-top: 1px solid rgba(255, 255, 255, 0.05);
  padding-top: 60px;
}

.logo-box-mini {
  width: 28px;
  height: 28px;
  background-color: var(--accent-green);
  border-radius: 6px;
  display: flex;
  align-items: center;
  justify-content: center;
  color: white;
  font-size: 14px;
}

.brand-name {
  font-size: 1.15rem;
  font-weight: 800;
  letter-spacing: 1px;
  color: #ffffff;
}

.footer-links-list li {
  margin-bottom: 12px;
}

.footer-link {
  color: #94a3b8;
  text-decoration: none;
  transition: all 0.3s ease;
  font-size: 14.5px;
  display: inline-block;
}

.footer-link:hover {
  color: var(--accent-green);
  transform: translateX(4px);
}

.newsletter-form .form-control {
  border-top-right-radius: 0 !important;
  border-bottom-right-radius: 0 !important;
  font-size: 14px;
}

.newsletter-form .btn {
  border-top-left-radius: 0 !important;
  border-bottom-left-radius: 0 !important;
  padding: 0 16px;
  display: flex;
  align-items: center;
  justify-content: center;
  box-shadow: none;
  background-color: var(--accent-green);
  border-color: var(--accent-green);
  color: white;
}

.form-input-glow {
  background-color: rgba(255, 255, 255, 0.03) !important;
  border: 1px solid rgba(255, 255, 255, 0.08) !important;
  color: white !important;
  border-radius: 8px !important;
}

.form-input-glow:focus {
  border-color: var(--accent-green) !important;
  box-shadow: 0 0 0 3px rgba(0, 185, 107, 0.2) !important;
}

.social-links-row {
  display: flex;
  gap: 12px;
}

.social-icon {
  width: 38px;
  height: 38px;
  background: rgba(255, 255, 255, 0.03);
  border: 1px solid rgba(255, 255, 255, 0.08);
  border-radius: 50%;
  display: flex;
  align-items: center;
  justify-content: center;
  color: #cbd5e1;
  text-decoration: none;
  transition: all 0.3s ease;
  font-size: 16px;
}

.social-icon:hover {
  color: white;
  transform: translateY(-3px);
  background: var(--accent-green);
  border-color: var(--accent-green);
  box-shadow: 0 5px 12px rgba(0, 185, 107, 0.35);
}

.footer-divider {
  border-color: rgba(255, 255, 255, 0.06);
  margin-top: 40px;
  margin-bottom: 25px;
}
</style>
