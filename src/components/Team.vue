<template>
  <section id="team" class="py-6 team-section">
    <!-- Glow Orb -->
    <div class="glow-orb glow-orb-team"></div>

    <div class="container">
      <div class="text-center mb-5">
        <div class="section-tag mb-2">TIM KAMI</div>
        <h2 class="display-6 fw-extrabold text-white">Di Balik Layar <span class="text-gradient">Vortex</span></h2>
        <p class="section-desc mt-2">Profesional berpengalaman dengan visi global yang siap mengakselerasi kesuksesan bisnis Anda.</p>
      </div>

      <div class="row g-4 justify-content-center">
        <div class="col-md-6 col-lg-3" v-for="member in team" :key="member.id">
          <div class="team-card glass-card">
            <div class="avatar-container mb-4">
              <div class="avatar-glow"></div>
              <div class="avatar-frame">
                <i :class="member.icon"></i>
              </div>
            </div>
            <h5 class="fw-bold mt-2 mb-1 text-white">{{ member.name }}</h5>
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
    description: 'Dengan pengalaman 15 tahun di industri teknologi global, Ahmad memimpin inovasi strategis Vortex.'
  },
  {
    id: 2,
    icon: 'bi bi-person-fill-slash',
    name: 'Siti Nurhaliza',
    position: 'Chief Technology Officer',
    description: 'Expert sistem cloud & cybersecurity bersertifikat AWS, mengawal keandalan seluruh infrastruktur.'
  },
  {
    id: 3,
    icon: 'bi bi-person-fill-check',
    name: 'Budi Santoso',
    position: 'Head of Product',
    description: 'Visioner produk dengan fokus kuat pada riset UX, mendedikasikan diri menciptakan solusi yang intuitif.'
  },
  {
    id: 4,
    icon: 'bi bi-person-fill-up',
    name: 'Rina Wijaya',
    position: 'Head of Sales',
    description: 'Menghubungkan inovasi dengan kebutuhan pasar, membantu ribuan klien bertransformasi secara digital.'
  }
];
</script>

<style scoped>
.team-section {
  background-color: #080f21;
  padding: 100px 0;
  position: relative;
  overflow: hidden;
}

.glow-orb-team {
  position: absolute;
  top: 10%;
  left: -5%;
  width: 350px;
  height: 350px;
  background: radial-gradient(circle, rgba(99, 102, 241, 0.08) 0%, rgba(0, 0, 0, 0) 70%);
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

.team-card {
  padding: 40px 30px;
  text-align: center;
  height: 100%;
  display: flex;
  flex-direction: column;
  align-items: center;
}

.avatar-container {
  position: relative;
  width: 100px;
  height: 100px;
}

.avatar-glow {
  position: absolute;
  top: 50%;
  left: 50%;
  transform: translate(-50%, -50%);
  width: 90%;
  height: 90%;
  background: radial-gradient(circle, rgba(6, 182, 212, 0.3) 0%, rgba(0, 0, 0, 0) 75%);
  filter: blur(8px);
  z-index: 1;
  border-radius: 50%;
  transition: all 0.3s ease;
}

.team-card:hover .avatar-glow {
  background: radial-gradient(circle, rgba(99, 102, 241, 0.5) 0%, rgba(0, 0, 0, 0) 75%);
  filter: blur(10px);
}

.avatar-frame {
  width: 100%;
  height: 100%;
  border-radius: 50%;
  border: 2px solid rgba(255, 255, 255, 0.08);
  background: rgba(15, 23, 42, 0.6);
  display: flex;
  align-items: center;
  justify-content: center;
  font-size: 42px;
  color: #06b6d4;
  position: relative;
  z-index: 2;
  transition: all 0.3s ease;
}

.team-card:hover .avatar-frame {
  border-color: #06b6d4;
  color: white;
  background: linear-gradient(135deg, #06b6d4 0%, #6366f1 100%);
  box-shadow: 0 0 15px rgba(6, 182, 212, 0.4);
}

.member-role {
  color: #38bdf8;
  font-size: 14px;
  font-weight: 600;
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

.social-btn:hover {
  background: rgba(6, 182, 212, 0.1);
  color: #06b6d4;
  border-color: #06b6d4;
  transform: scale(1.1) translateY(-2px);
  box-shadow: 0 5px 12px rgba(6, 182, 212, 0.2);
}

@media (max-width: 991px) {
  .team-section {
    padding: 60px 0;
  }
}
</style>
