<template>
  <section id="testimonials" class="py-5">
    <div class="container">
      <div class="text-center mb-5">
        <h2 class="display-5 fw-bold mb-3">Testimoni Klien</h2>
        <p class="fs-5 text-muted">Kepuasan klien adalah prioritas utama kami</p>
      </div>

      <div class="row g-4">
        <div class="col-md-6 col-lg-4" v-for="testimonial in testimonials" :key="testimonial.id">
          <div class="testimonial-card">
            <div class="stars mb-3">
              <i class="bi bi-star-fill" v-for="i in 5" :key="i"></i>
            </div>
            <p class="testimonial-text mb-4">{{ testimonial.text }}</p>
            <div class="d-flex align-items-center gap-3">
              <div class="client-avatar">
                <i class="bi bi-person-circle"></i>
              </div>
              <div>
                <h6 class="fw-bold mb-0">{{ testimonial.name }}</h6>
                <p class="text-muted small mb-0">{{ testimonial.company }}</p>
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
    text: 'Layanan yang diberikan sangat profesional dan memuaskan. Tim mereka sangat responsif dan memahami kebutuhan bisnis kami.',
    name: 'Hendra Kusuma',
    company: 'PT. Maju Jaya'
  },
  {
    id: 2,
    text: 'Implementasi solusi mereka meningkatkan efisiensi operasional kami hingga 40%. Sangat rekomendasikan!',
    name: 'Dewi Lestari',
    company: 'PT. Teknologi Nusantara'
  },
  {
    id: 3,
    text: 'Support yang luar biasa, selalu siap membantu 24/7. Partnership yang sangat berharga bagi bisnis kami.',
    name: 'Ricky Pratama',
    company: 'CV. Digital Indonesia'
  }
];
</script>

<style scoped>
.testimonial-card {
  background: white;
  border-radius: 15px;
  padding: 30px;
  box-shadow: 0 5px 20px rgba(0, 0, 0, 0.08);
  transition: all 0.3s ease;
  border-left: 4px solid #667eea;
}

.testimonial-card:hover {
  transform: translateY(-5px);
  box-shadow: 0 10px 30px rgba(0, 0, 0, 0.12);
}

.stars {
  color: #ffc107;
  font-size: 14px;
  letter-spacing: 2px;
}

.testimonial-text {
  color: #555;
  font-size: 15px;
  line-height: 1.6;
  font-style: italic;
}

.client-avatar {
  width: 45px;
  height: 45px;
  background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
  border-radius: 50%;
  display: flex;
  align-items: center;
  justify-content: center;
  color: white;
  font-size: 28px;
}
</style>
