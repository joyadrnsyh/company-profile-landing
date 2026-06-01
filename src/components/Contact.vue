<template>
  <section id="contact" class="py-5 bg-light">
    <div class="container">
      <div class="text-center mb-5">
        <h2 class="display-5 fw-bold mb-3">Hubungi Kami</h2>
        <p class="fs-5 text-muted">Kami siap menjawab pertanyaan Anda</p>
      </div>

      <div class="row g-4 mb-5">
        <div class="col-lg-4">
          <div class="contact-box">
            <div class="contact-icon">
              <i class="bi bi-geo-alt"></i>
            </div>
            <h5 class="fw-bold mb-2">Alamat</h5>
            <p class="text-muted">Jl. Merdeka No. 123<br />Jakarta, Indonesia 12345</p>
          </div>
        </div>
        <div class="col-lg-4">
          <div class="contact-box">
            <div class="contact-icon">
              <i class="bi bi-telephone"></i>
            </div>
            <h5 class="fw-bold mb-2">Telepon</h5>
            <p class="text-muted">+62 (21) 1234-5678<br />+62 821 9876 5432</p>
          </div>
        </div>
        <div class="col-lg-4">
          <div class="contact-box">
            <div class="contact-icon">
              <i class="bi bi-envelope"></i>
            </div>
            <h5 class="fw-bold mb-2">Email</h5>
            <p class="text-muted">info@company.com<br />support@company.com</p>
          </div>
        </div>
      </div>

      <div class="row">
        <div class="col-lg-8 mx-auto">
          <form @submit.prevent="handleSubmit">
            <div class="row g-3">
              <div class="col-md-6">
                <input type="text" class="form-control form-control-lg" placeholder="Nama Lengkap" required />
              </div>
              <div class="col-md-6">
                <input type="email" class="form-control form-control-lg" placeholder="Email" required />
              </div>
              <div class="col-12">
                <input type="text" class="form-control form-control-lg" placeholder="Subjek" required />
              </div>
              <div class="col-12">
                <textarea
                  class="form-control form-control-lg"
                  rows="5"
                  placeholder="Pesan Anda"
                  required
                ></textarea>
              </div>
              <div class="col-12">
                <button type="submit" class="btn btn-primary btn-lg w-100">
                  <i class="bi bi-send me-2"></i> Kirim Pesan
                </button>
              </div>
            </div>
          </form>
        </div>
      </div>
    </div>
  </section>
</template>

<script setup lang="ts">
function handleSubmit() {
  alert('Terima kasih! Pesan Anda telah terkirim.')
}
</script>

<style scoped>
.contact-box {
  background: white;
  border-radius: 15px;
  padding: 30px;
  text-align: center;
  box-shadow: 0 5px 20px rgba(0, 0, 0, 0.08);
  transition: all 0.3s ease;
}

.contact-box:hover {
  transform: translateY(-5px);
  box-shadow: 0 10px 30px rgba(0, 0, 0, 0.12);
}

.contact-icon {
  width: 60px;
  height: 60px;
  margin: 0 auto 20px;
  background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
  border-radius: 50%;
  display: flex;
  align-items: center;
  justify-content: center;
  font-size: 28px;
  color: white;
}

.form-control,
.form-control-lg {
  border: 1px solid #ddd;
  border-radius: 10px;
  padding: 12px 20px;
  font-size: 15px;
  transition: 0.3s;
}

.form-control:focus,
.form-control-lg:focus {
  border-color: #667eea;
  box-shadow: 0 0 0 0.2rem rgba(102, 126, 234, 0.25);
}

.btn-primary {
  background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
  border: none;
  font-weight: 600;
  transition: 0.3s;
}

.btn-primary:hover {
  transform: translateY(-3px);
  box-shadow: 0 10px 20px rgba(102, 126, 234, 0.3);
}
</style>
