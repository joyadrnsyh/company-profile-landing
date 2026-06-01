<template>
  <section id="services" class="py-6 services-section">
    <!-- Background Glow -->
    <div class="glow-orb glow-orb-services"></div>

    <div class="container">
      <div class="text-center mb-5">
        <div class="section-tag mb-2">LAYANAN KAMI</div>
        <h2 class="display-6 fw-extrabold text-white">Solusi Bisnis <span class="text-gradient">Profesional</span></h2>
        <p class="section-desc mt-2">Kami menyediakan berbagai layanan IT modern berkualitas tinggi untuk mendongkrak performa bisnis Anda.</p>
      </div>

      <div class="row g-4">
        <div class="col-md-6 col-lg-4" v-for="service in services" :key="service.id">
          <div class="service-card glass-card">
            <div class="service-icon-box mb-4">
              <i :class="service.icon"></i>
            </div>
            <h5 class="fw-bold mb-3 text-white">{{ service.title }}</h5>
            <p class="text-muted mb-4 small-text">{{ service.description }}</p>
            <a href="#contact" class="service-btn-link d-inline-flex align-items-center">
              Pelajari Lebih Lanjut <i class="bi bi-arrow-right ms-2 arrow-icon"></i>
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
    description: 'Kami membantu Anda merancang arsitektur dan memilih solusi teknologi terbaik yang sesuai dengan model bisnis Anda.'
  },
  {
    id: 2,
    icon: 'bi bi-graph-up',
    title: 'Analisis Data',
    description: 'Ubah data mentah bisnis Anda menjadi insight berharga yang dapat diandalkan untuk membuat keputusan strategis.'
  },
  {
    id: 3,
    icon: 'bi bi-cloud-check',
    title: 'Cloud Solution',
    description: 'Migrasi cloud yang mulus dan aman untuk meningkatkan skalabilitas, fleksibilitas, dan menghemat biaya operasional.'
  },
  {
    id: 4,
    icon: 'bi bi-shield-lock',
    title: 'Keamanan Data',
    description: 'Proteksi aset digital dan data pelanggan Anda dari serangan siber dengan standar pertahanan tingkat enterprise.'
  },
  {
    id: 5,
    icon: 'bi bi-chat-dots',
    title: 'Support Teknis',
    description: 'Tim engineer kami siap siaga 24/7 memantau sistem Anda dan menyelesaikan masalah teknis dengan respons kilat.'
  },
  {
    id: 6,
    icon: 'bi bi-graduation-cap',
    title: 'Pelatihan IT',
    description: 'Program peningkatan kompetensi terstruktur untuk mempersiapkan tim internal Anda menguasai teknologi terbaru.'
  }
];
</script>

<style scoped>
.services-section {
  background-color: #040711;
  padding: 100px 0;
  position: relative;
  overflow: hidden;
}

.glow-orb-services {
  position: absolute;
  bottom: 10%;
  right: -10%;
  width: 400px;
  height: 400px;
  background: radial-gradient(circle, rgba(168, 85, 247, 0.08) 0%, rgba(0, 0, 0, 0) 70%);
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
}

.section-desc {
  max-width: 600px;
  margin: 0 auto;
  color: #94a3b8;
  font-size: 15px;
}

.service-card {
  padding: 40px 30px;
  height: 100%;
  border-top: 3px solid rgba(255, 255, 255, 0.08) !important;
  display: flex;
  flex-direction: column;
  align-items: flex-start;
}

.service-card:hover {
  border-top: 3px solid #06b6d4 !important;
}

.service-icon-box {
  width: 54px;
  height: 54px;
  background: rgba(255, 255, 255, 0.03);
  border: 1px solid rgba(255, 255, 255, 0.08);
  border-radius: 12px;
  display: flex;
  align-items: center;
  justify-content: center;
  font-size: 24px;
  color: #06b6d4;
  transition: all 0.3s ease;
}

.service-card:hover .service-icon-box {
  background: linear-gradient(135deg, #06b6d4 0%, #6366f1 100%);
  color: white;
  border-color: transparent;
  box-shadow: 0 5px 15px rgba(6, 182, 212, 0.4);
}

.small-text {
  font-size: 14px;
  line-height: 1.6;
  flex-grow: 1;
}

.service-btn-link {
  color: #06b6d4;
  text-decoration: none;
  font-size: 14px;
  font-weight: 600;
  transition: all 0.3s ease;
}

.service-btn-link .arrow-icon {
  transition: transform 0.3s ease;
}

.service-card:hover .service-btn-link {
  color: #38bdf8;
}

.service-card:hover .service-btn-link .arrow-icon {
  transform: translateX(6px);
}

@media (max-width: 991px) {
  .services-section {
    padding: 60px 0;
  }
}
</style>
