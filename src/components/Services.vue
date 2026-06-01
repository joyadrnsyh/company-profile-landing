<template>
  <section id="services" class="py-5">
    <div class="container">
      <div class="text-center mb-5">
        <h2 class="display-5 fw-bold mb-3">Layanan Kami</h2>
        <p class="fs-5 text-muted">Kami menyediakan berbagai layanan profesional untuk memenuhi kebutuhan bisnis Anda</p>
      </div>

      <div class="row g-4">
        <div class="col-md-6 col-lg-4" v-for="service in services" :key="service.id">
          <div class="service-card">
            <div class="service-icon">
              <i :class="service.icon"></i>
            </div>
            <h5 class="fw-bold mb-3">{{ service.title }}</h5>
            <p class="text-muted mb-3">{{ service.description }}</p>
            <a href="#" class="btn-link">
              Pelajari Lebih Lanjut <i class="bi bi-arrow-right ms-2"></i>
            </a>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<script setup lang="ts">
const services = [
  {
    id: 1,
    icon: 'bi bi-laptop',
    title: 'Konsultasi IT',
    description: 'Kami membantu Anda memilih solusi teknologi yang tepat untuk bisnis Anda.'
  },
  {
    id: 2,
    icon: 'bi bi-graph-up',
    title: 'Analisis Data',
    description: 'Dapatkan insight berharga dari data bisnis Anda untuk pengambilan keputusan yang lebih baik.'
  },
  {
    id: 3,
    icon: 'bi bi-cloud-check',
    title: 'Cloud Solution',
    description: 'Solusi cloud terpercaya untuk meningkatkan fleksibilitas dan efisiensi bisnis Anda.'
  },
  {
    id: 4,
    icon: 'bi bi-shield-lock',
    title: 'Keamanan Data',
    description: 'Proteksi data bisnis Anda dengan solusi keamanan tingkat enterprise.'
  },
  {
    id: 5,
    icon: 'bi bi-chat-dots',
    title: 'Support Teknis',
    description: 'Tim support kami siap membantu Anda 24/7 untuk mengatasi masalah teknis.'
  },
  {
    id: 6,
    icon: 'bi bi-graduation-cap',
    title: 'Pelatihan',
    description: 'Program pelatihan komprehensif untuk meningkatkan skill tim Anda.'
  }
];
</script>

<style scoped>
.service-card {
  background: white;
  border-radius: 15px;
  padding: 30px;
  box-shadow: 0 5px 20px rgba(0, 0, 0, 0.08);
  transition: all 0.3s ease;
  height: 100%;
  border-top: 4px solid transparent;
}

.service-card:hover {
  transform: translateY(-10px);
  box-shadow: 0 15px 40px rgba(0, 0, 0, 0.15);
  border-top-color: #667eea;
}

.service-icon {
  width: 60px;
  height: 60px;
  background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
  border-radius: 10px;
  display: flex;
  align-items: center;
  justify-content: center;
  font-size: 28px;
  color: white;
  margin-bottom: 20px;
}

.btn-link {
  color: #667eea;
  text-decoration: none;
  font-weight: 600;
  transition: 0.3s;
}

.btn-link:hover {
  color: #764ba2;
  transform: translateX(5px);
  display: inline-block;
}
</style>
