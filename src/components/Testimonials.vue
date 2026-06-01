<template>
  <section id="testimonials" class="py-6 testimonials-section">
    <!-- Glow Orb -->
    <div class="glow-orb glow-orb-testimonials"></div>

    <div class="container">
      <div class="text-center mb-5">
        <div class="section-tag mb-2">TESTIMONI</div>
        <h2 class="display-6 fw-extrabold text-white">Apa Kata <span class="text-gradient">Klien Kami</span></h2>
        <p class="section-desc mt-2">Kepuasan dan kesuksesan bisnis klien adalah prioritas utama dan tolok ukur kesuksesan kami.</p>
      </div>

      <div class="row g-4">
        <div class="col-md-6 col-lg-4" v-for="testimonial in testimonials" :key="testimonial.id">
          <div class="testimonial-card glass-card position-relative overflow-hidden">
            <!-- Background Quote Symbol -->
            <div class="quote-bg-icon">
              <i class="bi bi-quote"></i>
            </div>
            
            <div class="stars mb-3">
              <i class="bi bi-star-fill" v-for="i in 5" :key="i"></i>
            </div>
            
            <p class="testimonial-text mb-4 text-white-50">{{ testimonial.text }}</p>
            
            <div class="d-flex align-items-center gap-3 profile-footer">
              <div class="client-avatar-frame">
                <i class="bi bi-person-fill text-cyan"></i>
              </div>
              <div>
                <h6 class="fw-bold mb-0 text-white">{{ testimonial.name }}</h6>
                <p class="company-text small mb-0">{{ testimonial.company }}</p>
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<script setup lang="ts">
const testimonials = [
  {
    id: 1,
    text: 'Layanan yang diberikan sangat profesional dan memuaskan. Tim engineer mereka sangat responsif dan memahami kebutuhan bisnis kami dengan detail.',
    name: 'Hendra Kusuma',
    company: 'PT. Maju Jaya'
  },
  {
    id: 2,
    text: 'Implementasi solusi cloud dari Vortex berhasil meningkatkan efisiensi biaya operasional server kami hingga 40%. Sangat direkomendasikan!',
    name: 'Dewi Lestari',
    company: 'PT. Teknologi Nusantara'
  },
  {
    id: 3,
    text: 'Dukungan teknis 24/7 mereka luar biasa, selalu siap sedia membantu kapan saja. Partnership ini sangat bernilai tinggi bagi ekosistem digital kami.',
    name: 'Ricky Pratama',
    company: 'CV. Digital Indonesia'
  }
];
</script>

<style scoped>
.testimonials-section {
  background-color: #040711;
  padding: 100px 0;
  position: relative;
  overflow: hidden;
}

.glow-orb-testimonials {
  position: absolute;
  top: 20%;
  right: -5%;
  width: 350px;
  height: 350px;
  background: radial-gradient(circle, rgba(6, 182, 212, 0.08) 0%, rgba(0, 0, 0, 0) 70%);
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

.testimonial-card {
  padding: 40px 30px;
  border-left: 4px solid #06b6d4 !important;
  height: 100%;
  display: flex;
  flex-direction: column;
  justify-content: space-between;
}

.testimonial-card:hover {
  border-left-color: #6366f1 !important;
}

.quote-bg-icon {
  position: absolute;
  top: -10px;
  right: 15px;
  font-size: 110px;
  color: rgba(255, 255, 255, 0.03);
  pointer-events: none;
  line-height: 1;
}

.stars {
  color: #fbbf24;
  font-size: 14px;
  letter-spacing: 2px;
}

.testimonial-text {
  font-size: 14.5px;
  line-height: 1.6;
  font-style: italic;
  position: relative;
  z-index: 2;
  flex-grow: 1;
}

.profile-footer {
  position: relative;
  z-index: 2;
  margin-top: 15px;
}

.client-avatar-frame {
  width: 42px;
  height: 42px;
  background: rgba(6, 182, 212, 0.1);
  border: 1px solid rgba(6, 182, 212, 0.2);
  border-radius: 50%;
  display: flex;
  align-items: center;
  justify-content: center;
  font-size: 20px;
}

.text-cyan {
  color: #06b6d4;
}

.company-text {
  color: #38bdf8;
  font-weight: 500;
}

@media (max-width: 991px) {
  .testimonials-section {
    padding: 60px 0;
  }
}
</style>
