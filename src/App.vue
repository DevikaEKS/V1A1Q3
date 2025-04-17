<script setup>
const techData = [
  {
    title: "Data Scientist",
    description: "Data scientists gather and analyze large sets of structured and unstructured data.",
    img: "https://cdn-icons-png.flaticon.com/512/4140/4140048.png",
    borderColor: "#f44336",
  },
  {
    title: "IOT Developer",
    description: "Developers are professionals who can develop, manage, and monitor IoT devices.",
    img: "https://cdn-icons-png.flaticon.com/512/3176/3176299.png",
    borderColor: "#03a9f4",
  },
  {
    title: "VR Developer",
    description: "A VR developer creates completely new digital experiences that feel real.",
    img: "https://cdn-icons-png.flaticon.com/512/4280/4280496.png",
    borderColor: "#673ab7",
  },
  {
    title: "ML Engineer",
    description: "Machine learning engineers feed data into models to make predictions or decisions.",
    img: "https://cdn-icons-png.flaticon.com/512/4386/4386222.png",
    borderColor: "#ff9800",
  }
];
</script>

<template>
  <main>
    <div class="technologies-container">
      <div class="techpart">
        <h2 class="tech-heading">Learn 4.0 Technologies</h2>
        <p class="tech-subtext">
          Get trained by alumni of IITs and top companies like Amazon, Microsoft, Intel,
          Nvidia, Qualcomm, etc. Learn directly from professionals involved in Product
          Development.
        </p>

        <div class="tech-grid">
          <div
            v-for="(tech, index) in techData"
            :key="index"
            class="tech-card"
            :style="{ borderTop: `4px solid ${tech.borderColor}` }"
          >
            <h3 class="tech-title">{{ tech.title }}</h3>
            <p class="tech-desc">{{ tech.description }}</p>
            <img :src="tech.img" :alt="tech.title" class="tech-img" />
          </div>
        </div>
      </div>
    </div>
  </main>
</template>
