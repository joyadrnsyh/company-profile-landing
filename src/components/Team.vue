<template>
  <section id="team" class="py-5 bg-light">
    <div class="container">
      <div class="text-center mb-5">
        <h2 class="display-5 fw-bold mb-3">Tim Kami</h2>
        <p class="fs-5 text-muted">Profesional berpengalaman siap melayani Anda</p>
      </div>

      <div class="row g-4">
        <div class="col-md-6 col-lg-3" v-for="member in team" :key="member.id">
          <div class="team-card">
            <div class="team-image">
              <i :class="member.icon"></i>
            </div>
            <h5 class="fw-bold mt-3 mb-1">{{ member.name }}</h5>
            <p class="text-primary fw-500 small mb-2">{{ member.position }}</p>
            <p class="text-muted small mb-3">{{ member.description }}</p>
            <div class="social-links">
              <a href="#" class="social-link"><i class="bi bi-linkedin"></i></a>
              <a href="#" class="social-link"><i class="bi bi-twitter"></i></a>
              <a href="#" class="social-link"><i class="bi bi-envelope"></i></a>
            </div>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<script setup lang="ts">
const team = [
  {
    id: 1,
    icon: 'bi bi-person-circle',
    name: 'Ahmad Rahman',
    position: 'CEO & Founder',
    description: 'Dengan pengalaman 15 tahun, Ahmad memimpin perusahaan menuju kesuksesan.'
  },
  {
    id: 2,
    icon: 'bi bi-person-circle',
    name: 'Siti Nurhaliza',
    position: 'Chief Technology Officer',
    description: 'Expert dalam teknologi cloud dan infrastructure.'
  },
  {
    id: 3,
    icon: 'bi bi-person-circle',
    name: 'Budi Santoso',
    position: 'Head of Product',
    description: 'Visioner dalam mengembangkan produk inovatif.'
  },
  {
    id: 4,
    icon: 'bi bi-person-circle',
    name: 'Rina Wijaya',
    position: 'Head of Sales',
    description: 'Profesional sales dengan track record yang cemerlang.'
  }
];
</script>

<style scoped>
.team-card {
  background: white;
  border-radius: 15px;
  padding: 30px;
  text-align: center;
  box-shadow: 0 5px 20px rgba(0, 0, 0, 0.08);
  transition: all 0.3s ease;
}

.team-card:hover {
  transform: translateY(-10px);
  box-shadow: 0 15px 40px rgba(0, 0, 0, 0.15);
}

.team-image {
  width: 100px;
  height: 100px;
  margin: 0 auto 20px;
  background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
  border-radius: 50%;
  display: flex;
  align-items: center;
  justify-content: center;
  font-size: 50px;
  color: white;
}

.social-links {
  display: flex;
  gap: 10px;
  justify-content: center;
}

.social-link {
  width: 35px;
  height: 35px;
  background: #f0f0f0;
  border-radius: 50%;
  display: flex;
  align-items: center;
  justify-content: center;
  color: #667eea;
  text-decoration: none;
  transition: 0.3s;
}

.social-link:hover {
  background: #667eea;
  color: white;
  transform: scale(1.1);
}
</style>
