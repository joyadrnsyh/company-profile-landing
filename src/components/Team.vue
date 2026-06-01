<template>
  <section id="team" class="py-6 team-section">
    <!-- Background shape -->
    <div class="team-shape-circle"></div>

    <div class="container">
      <div class="text-center mb-5">
        <div class="tp-section-tag mb-2">Our Team</div>
        <h2 class="tp-section-title display-6">Meet Our Expert <span class="text-green">Advisors</span></h2>
        <p class="section-desc mt-2">Profesional berpengalaman yang siap membantu menganalisis kebutuhan proteksi bisnis dan pribadi Anda.</p>
      </div>

      <div class="row g-4 justify-content-center">
        <div class="col-md-6 col-lg-3" v-for="member in team" :key="member.id">
          <div class="team-card tp-card">
            <div class="avatar-container mb-4">
              <div class="avatar-frame">
                <i :class="member.icon"></i>
              </div>
            </div>
            <h5 class="fw-bold mt-2 mb-1 text-dark">{{ member.name }}</h5>
            <p class="member-role mb-3">{{ member.position }}</p>
            <p class="text-muted small mb-4 card-desc">{{ member.description }}</p>
            <div class="social-links-container">
              <a href="#" class="social-btn"><i class="bi bi-linkedin"></i></a>
              <a href="#" class="social-btn"><i class="bi bi-twitter-x"></i></a>
              <a href="#" class="social-btn"><i class="bi bi-envelope-fill"></i></a>
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
    icon: 'bi bi-person-fill-gear',
    name: 'Ahmad Rahman',
    position: 'CEO & Founder',
    description: 'Dengan pengalaman 15 tahun di industri asuransi global, Ahmad memimpin inovasi strategis Vortex.'
  },
  {
    id: 2,
    icon: 'bi bi-person-fill-slash',
    name: 'Siti Nurhaliza',
    position: 'Chief Technology Officer',
    description: 'Expert sistem proteksi data & cloud security, memastikan seluruh platform asuransi aman.'
  },
  {
    id: 3,
    icon: 'bi bi-person-fill-check',
    name: 'Budi Santoso',
    position: 'Head of Product',
    description: 'Menciptakan produk asuransi cerdas dan digital yang mudah digunakan oleh nasabah.'
  },
  {
    id: 4,
    icon: 'bi bi-person-fill-up',
    name: 'Rina Wijaya',
    position: 'Head of Sales',
    description: 'Mendedikasikan diri membantu ribuan keluarga dan perusahaan memilih polis yang tepat.'
  }
];
</script>

<style scoped>
.team-section {
  background-color: var(--bg-primary);
  padding: 100px 0;
  position: relative;
  overflow: hidden;
}

.team-shape-circle {
  position: absolute;
  top: 10%;
  right: -5%;
  width: 350px;
  height: 350px;
  background: radial-gradient(circle, rgba(0, 185, 107, 0.03) 0%, rgba(255, 255, 255, 0) 70%);
  pointer-events: none;
}

.section-desc {
  max-width: 600px;
  margin: 0 auto;
  color: var(--text-muted);
  font-size: 15px;
}

.team-card {
  text-align: center;
  display: flex;
  flex-direction: column;
  align-items: center;
  height: 100%;
}

.avatar-container {
  position: relative;
  width: 100px;
  height: 100px;
}

.avatar-frame {
  width: 100%;
  height: 100%;
  border-radius: 50%;
  border: 2px solid rgba(0, 185, 107, 0.15);
  background: #e6f8f0;
  display: flex;
  align-items: center;
  justify-content: center;
  font-size: 42px;
  color: var(--accent-green);
  transition: all 0.3s ease;
}

.team-card:hover .avatar-frame {
  background-color: var(--accent-green);
  color: white;
  border-color: var(--accent-green);
  box-shadow: 0 0 15px rgba(0, 185, 107, 0.25);
  transform: rotateY(180deg);
}

.member-role {
  color: var(--accent-green);
  font-size: 14px;
  font-weight: 700;
  letter-spacing: 0.5px;
}

.card-desc {
  font-size: 13.5px;
  line-height: 1.5;
  flex-grow: 1;
}

.social-links-container {
  display: flex;
  gap: 12px;
  justify-content: center;
  margin-top: auto;
}

.social-btn {
  width: 36px;
  height: 36px;
  background: #f8fafc;
  border: 1px solid rgba(15, 23, 42, 0.08);
  border-radius: 50%;
  display: flex;
  align-items: center;
  justify-content: center;
  color: var(--text-muted);
  text-decoration: none;
  transition: all 0.3s ease;
  font-size: 15px;
}

.social-btn:hover {
  background: var(--accent-green);
  color: white;
  border-color: var(--accent-green);
  transform: translateY(-2px);
  box-shadow: 0 4px 10px rgba(0, 185, 107, 0.2);
}

.text-green {
  color: var(--accent-green) !important;
}

@media (max-width: 991px) {
  .team-section {
    padding: 60px 0;
  }
}
</style>
