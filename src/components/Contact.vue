<template>
  <section id="contact" class="py-6 contact-section">
    <!-- Glow Orb -->
    <div class="glow-orb glow-orb-contact"></div>

    <div class="container">
      <div class="text-center mb-5">
        <div class="section-tag mb-2">HUBUNGI KAMI</div>
        <h2 class="display-6 fw-extrabold text-white">Mari Mulai <span class="text-gradient">Kolaborasi</span></h2>
        <p class="section-desc mt-2">Punya pertanyaan atau proyek kerja sama? Hubungi tim ahli kami sekarang juga.</p>
      </div>

      <div class="row g-4 mb-5">
        <div class="col-lg-4">
          <div class="contact-box glass-card">
            <div class="contact-icon-box mb-3">
              <i class="bi bi-geo-alt-fill"></i>
            </div>
            <h5 class="fw-bold mb-2 text-white">Alamat Kantor</h5>
            <p class="text-muted small-text mb-0">Jl. Merdeka No. 123<br />Jakarta, Indonesia 12345</p>
          </div>
        </div>
        <div class="col-lg-4">
          <div class="contact-box glass-card">
            <div class="contact-icon-box mb-3">
              <i class="bi bi-telephone-fill"></i>
            </div>
            <h5 class="fw-bold mb-2 text-white">Kontak Langsung</h5>
            <p class="text-muted small-text mb-0">+62 (21) 1234-5678<br />+62 821 9876 5432</p>
          </div>
        </div>
        <div class="col-lg-4">
          <div class="contact-box glass-card">
            <div class="contact-icon-box mb-3">
              <i class="bi bi-envelope-fill"></i>
            </div>
            <h5 class="fw-bold mb-2 text-white">Email Resmi</h5>
            <p class="text-muted small-text mb-0">info@vortexsolutions.com<br />support@vortexsolutions.com</p>
          </div>
        </div>
      </div>

      <div class="row">
        <div class="col-lg-8 mx-auto">
          <div class="form-wrapper glass-card p-4 p-md-5">
            <form @submit.prevent="handleSubmit">
              <div class="row g-3">
                <div class="col-md-6">
                  <label class="form-label text-white small fw-600 mb-1">Nama Lengkap</label>
                  <input type="text" class="form-control form-input-glow form-control-lg" placeholder="Masukkan nama lengkap Anda" required />
                </div>
                <div class="col-md-6">
                  <label class="form-label text-white small fw-600 mb-1">Alamat Email</label>
                  <input type="email" class="form-control form-input-glow form-control-lg" placeholder="nama@email.com" required />
                </div>
                <div class="col-12">
                  <label class="form-label text-white small fw-600 mb-1">Subjek Pesan</label>
                  <input type="text" class="form-control form-input-glow form-control-lg" placeholder="Topik konsultasi / proyek" required />
                </div>
                <div class="col-12">
                  <label class="form-label text-white small fw-600 mb-1">Detail Pesan</label>
                  <textarea
                    class="form-control form-input-glow form-control-lg"
                    rows="5"
                    placeholder="Tuliskan detail kebutuhan bisnis atau pertanyaan Anda di sini..."
                    required
                  ></textarea>
                </div>
                <div class="col-12 mt-4">
                  <button type="submit" class="btn btn-glow-primary btn-lg w-100 py-3">
                    <i class="bi bi-send-fill me-2"></i> Kirim Pesan Sekarang
                  </button>
                </div>
              </div>
            </form>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<script setup lang="ts">
function handleSubmit() {
  alert('Terima kasih! Pesan Anda telah terkirim. Tim kami akan segera menghubungi Anda kembali.')
}
</script>

<style scoped>
.contact-section {
  background-color: #080f21;
  padding: 100px 0;
  position: relative;
  overflow: hidden;
}

.glow-orb-contact {
  position: absolute;
  bottom: -5%;
  left: 20%;
  width: 450px;
  height: 450px;
  background: radial-gradient(circle, rgba(99, 102, 241, 0.08) 0%, rgba(0, 0, 0, 0) 70%);
  filter: blur(80px);
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
}

.section-desc {
  max-width: 600px;
  margin: 0 auto;
  color: #94a3b8;
  font-size: 15px;
}

.contact-box {
  padding: 35px 30px;
  text-align: center;
  height: 100%;
  display: flex;
  flex-direction: column;
  align-items: center;
}

.contact-icon-box {
  width: 52px;
  height: 52px;
  background: rgba(6, 182, 212, 0.1);
  border: 1px solid rgba(6, 182, 212, 0.2);
  border-radius: 50%;
  display: flex;
  align-items: center;
  justify-content: center;
  font-size: 24px;
  color: #06b6d4;
  transition: all 0.3s ease;
}

.contact-box:hover .contact-icon-box {
  background: linear-gradient(135deg, #06b6d4 0%, #6366f1 100%);
  color: white;
  border-color: transparent;
  box-shadow: 0 0 15px rgba(6, 182, 212, 0.4);
}

.small-text {
  font-size: 14.5px;
  line-height: 1.6;
}

.form-wrapper {
  background: rgba(16, 23, 41, 0.4);
  border: 1px solid rgba(255, 255, 255, 0.05);
}

.form-wrapper:hover {
  transform: none;
  box-shadow: 0 15px 35px rgba(0, 0, 0, 0.3);
  border-color: rgba(255, 255, 255, 0.08);
}

.fw-600 {
  font-weight: 600;
}

@media (max-width: 991px) {
  .contact-section {
    padding: 60px 0;
  }
}
</style>
