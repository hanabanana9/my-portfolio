<template>
  <div class="portfolio-showcase">
    <div class="project-card" v-for="project in projects" :key="project.id">
      <img :src="project.image" :alt="`${project.title} Image`" class="project-image" />
      <h3 class="project-title">{{ project.title }}</h3>
      <p class="project-description">{{ project.description }}</p>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      projects: [
        {
          id: 1,
          title: "WebFit: Online System on Gym Utilization Reservation and Coach Appointment",
          description: "A web-based platform designed to simplify the process of booking coaching sessions at a gym. It aims to reduce waiting times for customers by allowing them to schedule appointments online, eliminating the need for phone calls or in-person visits.",
          image: require('@/assets/pnr.png'),
        },
        {
          id: 2,
          title: "AquaTect: Innovative Design of an AI-Driven System for Crayfish Gender Detection",
          description: "AquaTect is an AI-driven system that automates the gender detection of live crayfish, improving accuracy and efficiency compared to manual methods. This technology enhances crayfish farming by enabling faster, more precise sorting for sustainable aquaculture.",
          image: require('@/assets/spp.png'),
        },
      ],
    };
  },
};
</script>

<style scoped>
.portfolio-showcase {
  display: flex;
  flex-wrap: wrap;
  gap: 24px;
  justify-content: center;
  padding: 24px;
}

.project-card {
  background: #f3e8ff; /* Light purple background */
  border: 2px solid #a855f7; /* Deep purple border */
  border-radius: 12px;
  box-shadow: 0 6px 10px rgba(0, 0, 0, 0.15);
  padding: 24px;
  max-width: 350px; /* Slightly larger size */
  text-align: center;
  transition: transform 0.3s, box-shadow 0.3s;
}

.project-card:hover {
  transform: translateY(-8px);
  box-shadow: 0 8px 16px rgba(0, 0, 0, 0.2);
}

.project-image {
  max-width: 100%;
  border-radius: 12px;
  margin-bottom: 20px;
}

.project-title {
  font-size: 1.5rem; /* Slightly larger text */
  font-weight: 700;
  color: #6b21a8; /* Bold deep purple */
  margin: 12px 0;
}

.project-description {
  font-size: 1rem; /* Bigger description font */
  color: #4c1d95; /* Muted purple */
  text-align: justify; /* Justify the text */
  margin-bottom: 16px; /* Adjust margin for better spacing */
}
</style>
