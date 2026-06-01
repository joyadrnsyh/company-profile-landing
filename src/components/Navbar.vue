<template>
  <nav class="navbar navbar-expand-lg navbar-light bg-white shadow-sm sticky-top">
    <div class="container">
      <a class="navbar-brand fw-bold fs-4" href="#home">
        <i class="bi bi-building text-primary"></i> Company
      </a>
      <button
        class="navbar-toggler"
        type="button"
        data-bs-toggle="collapse"
        data-bs-target="#navbarNav"
        aria-controls="navbarNav"
        aria-expanded="false"
        aria-label="Toggle navigation"
      >
        <span class="navbar-toggler-icon"></span>
      </button>
      <div class="collapse navbar-collapse" id="navbarNav">
        <ul class="navbar-nav ms-auto gap-2">
          <li class="nav-item">
            <a class="nav-link active fw-500" href="#home">Home</a>
          </li>
          <li class="nav-item">
            <a class="nav-link fw-500" href="#about">Tentang Kami</a>
          </li>
          <li class="nav-item">
            <a class="nav-link fw-500" href="#services">Layanan</a>
          </li>
          <li class="nav-item">
            <a class="nav-link fw-500" href="#team">Tim</a>
          </li>
          <li class="nav-item">
            <a class="nav-link fw-500" href="#testimonials">Testimoni</a>
          </li>
          <li class="nav-item">
            <a class="nav-link fw-500" href="#contact">Hubungi Kami</a>
          </li>
          <li class="nav-item">
            <button class="btn btn-primary btn-sm px-3">Daftar</button>
          </li>
        </ul>
      </div>
    </div>
  </nav>
</template>

<style scoped>
.nav-link {
  color: #6c757d;
  transition: 0.3s;
}

.nav-link:hover,
.nav-link.active {
  color: #0d6efd;
  font-weight: 600;
}

.navbar-brand {
  color: #0d6efd;
  transition: 0.3s;
}

.navbar-brand:hover {
  transform: scale(1.05);
}
</style>
