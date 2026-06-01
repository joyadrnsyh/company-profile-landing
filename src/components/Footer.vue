<template>
  <footer class="footer">
    <div class="container py-5">
      <div class="row g-4 mb-5">
        <div class="col-md-3">
          <h5 class="fw-bold mb-3">Company</h5>
          <ul class="list-unstyled">
            <li><a href="#" class="footer-link">Tentang Kami</a></li>
            <li><a href="#" class="footer-link">Blog</a></li>
            <li><a href="#" class="footer-link">Karir</a></li>
            <li><a href="#" class="footer-link">Press</a></li>
          </ul>
        </div>
        <div class="col-md-3">
          <h5 class="fw-bold mb-3">Layanan</h5>
          <ul class="list-unstyled">
            <li><a href="#" class="footer-link">Konsultasi IT</a></li>
            <li><a href="#" class="footer-link">Cloud Solution</a></li>
            <li><a href="#" class="footer-link">Keamanan Data</a></li>
            <li><a href="#" class="footer-link">Support Teknis</a></li>
          </ul>
        </div>
        <div class="col-md-3">
          <h5 class="fw-bold mb-3">Dukungan</h5>
          <ul class="list-unstyled">
            <li><a href="#" class="footer-link">Help Center</a></li>
            <li><a href="#" class="footer-link">Documentation</a></li>
            <li><a href="#" class="footer-link">Status</a></li>
            <li><a href="#" class="footer-link">Contact</a></li>
          </ul>
        </div>
        <div class="col-md-3">
          <h5 class="fw-bold mb-3">Ikuti Kami</h5>
          <div class="social-links">
            <a href="#" class="social-icon"><i class="bi bi-facebook"></i></a>
            <a href="#" class="social-icon"><i class="bi bi-twitter"></i></a>
            <a href="#" class="social-icon"><i class="bi bi-linkedin"></i></a>
            <a href="#" class="social-icon"><i class="bi bi-instagram"></i></a>
          </div>
        </div>
      </div>

      <hr class="my-4" />

      <div class="row align-items-center">
        <div class="col-md-6">
          <p class="text-muted mb-0">&copy; 2024 Company. All rights reserved.</p>
        </div>
        <div class="col-md-6 text-md-end">
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

<style scoped>
.footer {
  background: #2d3436;
  color: #dfe6e9;
  margin-top: 80px;
}

.footer h5 {
  color: white;
}

.footer-link {
  color: #dfe6e9;
  text-decoration: none;
  transition: 0.3s;
  font-size: 14px;
}

.footer-link:hover {
  color: #667eea;
  padding-left: 5px;
}

.social-links {
  display: flex;
  gap: 15px;
}

.social-icon {
  width: 40px;
  height: 40px;
  background: rgba(102, 126, 234, 0.2);
  border-radius: 50%;
  display: flex;
  align-items: center;
  justify-content: center;
  color: #667eea;
  text-decoration: none;
  transition: 0.3s;
  font-size: 18px;
}

.social-icon:hover {
  background: #667eea;
  color: white;
  transform: translateY(-3px);
}

hr {
  border-color: rgba(255, 255, 255, 0.1);
}
</style>
