<template>
  <div class="creative-page">
    <h2>My Hobbies</h2>
    <ul class="hobby-list">
      <li v-for="(hobby, index) in hobbies" :key="index" class="hobby-item">
        <div class="hobby-info">
          <h3>{{ hobby.name }}</h3>
          <p class="justified-text">{{ hobby.description }}</p>
        </div>
      </li>
    </ul>
  </div>
</template>

<script>
export default {
  data() {
    return {
      hobbies: [
        {
          name: 'Photography',
          description: 'Photography lets me capture unique moments and explore different perspectives. Whether it’s nature, portraits, or street photography, each shot helps me learn new techniques and appreciate the beauty around me. It is fulfilling to look back at my photos and see how I have grown.',
        },
        {
          name: 'Watching Movies',
          description: 'Watching movies is my way of escaping into different worlds and stories. It allows me to relax and unwind while exploring various genres like action, drama, or comedy. I enjoy sharing the experience with friends, sparking conversations about the films and their themes.',
        },
        {
          name: 'Playing Mobile Games',
          description: 'Mobile gaming is a fun way to challenge myself and relax on the go. From quick puzzles to competitive games, it offers endless entertainment. I enjoy connecting with others in multiplayer games and improving my skills with every session.',
        },
      ],
    };
  },
};
</script>

<style scoped>
/* Import a modern, elegant font */
@import url('https://fonts.googleapis.com/css2?family=Montserrat:wght@400;600&display=swap');

body {
  margin: 0;
  font-family: 'Montserrat', sans-serif;
  background-color: #f5f5f5;
}

.creative-page {
  max-width: 900px;
  margin: 50px auto;
  padding: 30px;
  background-color: #ffffff;
  border-radius: 16px;
  box-shadow: 0 8px 20px rgba(0, 0, 0, 0.1);
  text-align: center;
}

h2 {
  font-size: 2.5rem;
  margin-bottom: 30px;
  color: #4a148c; /* Rich purple */
  font-weight: 600;
  letter-spacing: 1px;
}

.hobby-list {
  list-style: none;
  padding: 0;
  margin: 0;
}

.hobby-item {
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
  background: linear-gradient(135deg, #e1bee7, #ce93d8); /* Gradient for hobby cards */
  border-radius: 12px;
  padding: 20px;
  margin-bottom: 20px;
  color: #311b92; /* Deep purple for text */
  transition: transform 0.3s, box-shadow 0.3s ease;
  box-shadow: 0 4px 10px rgba(0, 0, 0, 0.15);
}

.hobby-item:hover {
  transform: translateY(-5px);
  box-shadow: 0 12px 25px rgba(0, 0, 0, 0.25);
}

.hobby-info h3 {
  margin: 0;
  font-size: 1.8rem;
  font-weight: 600;
}

.hobby-info p {
  margin-top: 10px;
  font-size: 1rem;
  font-weight: 400;
  color: #4e4e4e;
}

.justified-text {
  text-align: justify;
  text-justify: inter-word;
}

@media (max-width: 768px) {
  .creative-page {
    padding: 20px;
  }

  h2 {
    font-size: 2rem;
  }

  .hobby-info h3 {
    font-size: 1.5rem;
  }

  .hobby-info p {
    font-size: 0.95rem;
  }
}
</style>
