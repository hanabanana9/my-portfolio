<template>
  <div class="profile-page">
    <div class="profile-card">
      <div class="profile-image">
        <img :src="photo" alt="Profile Picture" />
      </div>
      <div class="profile-details">
        <h2>{{ name }}</h2>
        <p class="bio">{{ bio }}</p>
        <div class="social-links">
          <a :href="social.facebook" target="_blank" rel="noopener">
            <i class="fab fa-facebook"></i>
          </a>
          <a :href="social.instagram" target="_blank" rel="noopener">
            <i class="fab fa-instagram"></i>
          </a>
          <a :href="social.twitter" target="_blank" rel="noopener">
            <i class="fab fa-twitter"></i>
          </a>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      name: "Hannah T. Cancino",
      bio: "I am a Computer Engineering graduate from the Technological Institute of the Philippines. I am passionate about utilizing technology to deliver impactful solutions. With a strong dedication to excellence and attention to detail, I aim to contribute to organizations by applying my technical knowledge and problem-solving skills. I am eager to thrive in a professional setting that values collaboration and innovation.",
      photo: require('@/assets/pic.jpeg'),
      social: {
        facebook: "https://www.facebook.com/hannah.cancinoo?mibextid=LQQJ4d&mibextid=LQQJ4d",
        instagram: "https://www.instagram.com/hannah.cancino/",
        twitter: "https://x.com/hanabananaxx_?s=21",
      },
    };
  },
};
</script>

<style scoped>
/* Import font for clean and elegant typography */
@import url('https://fonts.googleapis.com/css2?family=Roboto:wght@400;700&display=swap');

.profile-page {
  min-height: 100vh;
  background: linear-gradient(135deg, #7201a8, #d49ddf); /* Purple gradient */
  display: flex;
  align-items: center;
  justify-content: center;
  font-family: 'Roboto', sans-serif;
}

.profile-card {
  max-width: 600px;
  width: 100%;
  background-color: #f8e7fb; /* Soft purple background */
  border: 2px solid #a755c7; /* Vibrant purple border */
  border-radius: 16px; /* Rounded corners */
  box-shadow: 0 8px 15px rgba(114, 1, 168, 0.2); /* Subtle purple shadow */
  padding: 40px;
  text-align: center;
}

.profile-image {
  background-color: #a755c7; /* Darker purple for contrast */
  border-radius: 12px; /* Matches the square corners */
  padding: 10px;
  margin-bottom: 25px;
}

.profile-image img {
  width: 160px;
  height: 160px;
  border-radius: 8px; /* Slight rounding for square picture */
  object-fit: cover;
  border: 4px solid #f8e7fb; /* Soft purple border */
  box-shadow: 0 5px 10px rgba(114, 1, 168, 0.3);
}

.profile-details h2 {
  font-size: 1.8rem;
  color: #7201a8; /* Bold purple */
  margin-bottom: 15px;
}

.profile-details p {
  font-size: 1rem;
  color: #333; /* Neutral gray for readability */
  line-height: 1.6; /* Improved readability with larger line spacing */
  margin-bottom: 25px;
  text-align: justify;
}

.social-links {
  display: flex;
  justify-content: center;
  gap: 20px;
}

.social-links a {
  font-size: 30px; /* Bigger size for social icons */
  color: #7201a8; /* Deep purple for icons */
  transition: transform 0.3s ease, color 0.3s ease;
}

.social-links a:hover {
  color: #d49ddf; /* Lighter purple on hover */
  transform: scale(1.2); /* Zoom effect */
}

/* Responsive Design */
@media (max-width: 768px) {
  .profile-card {
    padding: 30px;
  }

  .profile-details h2 {
    font-size: 1.5rem;
  }

  .profile-details p {
    font-size: 0.9rem;
  }

  .social-links a {
    font-size: 26px;
  }
}
</style>
