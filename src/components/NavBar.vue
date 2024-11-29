<template>
  <nav class="navbar">
    <div class="navbar-logo">
      <h1>My Portfolio</h1>
    </div>
    <ul class="navbar-links">
      <li>
        <router-link to="/portfolio/profile">Profile</router-link>
      </li>
      <li>
        <router-link to="/portfolio/showcase">Showcase</router-link>
      </li>
      <li>
        <router-link to="/portfolio/contact">Contact</router-link>
      </li>
      <li>
        <router-link to="/portfolio/creative">Creative</router-link>
      </li>
      <li>
        <router-link to="/login">Logout</router-link>
      </li>
    </ul>
  </nav>
</template>

<script>
export default {
  name: "NavBar",
};
</script>

<style scoped>
.navbar {
  background-color: #f3e8ff; /* Light purple */
  border: 3px solid #a855f7; /* Deep purple border */
  border-radius: 12px; /* Rounded corners */
  padding: 1rem 2rem;
  display: flex;
  justify-content: space-between;
  align-items: center;
  color: #6b21a8; /* Deep purple text */
  box-shadow: 0 4px 8px rgba(0, 0, 0, 0.1); /* Subtle shadow */
}

.navbar-logo h1 {
  margin: 0;
  font-size: 1.8rem;
  font-family: "Poppins", sans-serif; /* Modern font */
  color: #6b21a8;
}

.navbar-links {
  list-style: none;
  display: flex;
  gap: 1.5rem;
  margin: 0;
  padding: 0;
}

.navbar-links li {
  display: inline;
}

.navbar-links a {
  color: #6b21a8; /* Deep purple text */
  text-decoration: none;
  font-size: 1rem;
  font-family: "Poppins", sans-serif;
  padding: 0.5rem 1rem;
  border-radius: 8px;
  transition: background-color 0.3s, color 0.3s;
}

.navbar-links a:hover {
  background-color: #a855f7; /* Deep purple hover background */
  color: white; /* Contrast text */
  transform: scale(1.1); /* Slight zoom effect */
}

@media (max-width: 768px) {
  .navbar {
    flex-direction: column;
    align-items: flex-start;
  }

  .navbar-links {
    flex-direction: column;
    gap: 1rem;
    width: 100%;
    margin-top: 1rem;
  }

  .navbar-links a {
    width: 100%;
    text-align: left;
  }
}
</style>
