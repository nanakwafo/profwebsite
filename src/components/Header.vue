<template>
  <header class="header">
    <h1 class="name">Nana Mensah</h1>
    <p class="title">Software, DevOps & Cloud Engineer</p>
    <img src="/profile.jpg" alt="Nana Mensah" class="profile-pic" />
  </header>
</template>

<style scoped>
.header {
  position: sticky;
  top: 0;
  z-index: 1000;
  background-color: #1e1e1e;
  color: white;
  padding: 2rem 1rem;
  text-align: center;
  border-bottom: 2px solid #1a73e8;
  box-shadow: 0 2px 8px rgba(0, 0, 0, 0.2);
}

/* Optional: Responsive typography */
.name {
  font-size: 2rem;
  font-weight: 700;
  margin-bottom: 0.5rem;
  letter-spacing: 0.5px;
}

.title {
  font-size: 1.2rem;
  color: #ccc;
}
.profile-pic {
  width: 120px;
  height: 120px;
  border-radius: 50%;
  object-fit: cover;
  margin-bottom: 1rem;
  border: 3px solid #1a73e8;
}
</style>
