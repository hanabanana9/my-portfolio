<template>
  <footer class="footer">
    <div class="footer-content">
      <p class="footer-text">&copy; 2024 Hannah's Portfolio. All rights reserved.</p>
      <div class="footer-social">
        <a href="https://www.facebook.com/hannah.cancinoo?mibextid=LQQJ4d&mibextid=LQQJ4d" target="_blank" rel="noopener noreferrer">
        </a>
        <a href="instagram.com/hannah.cancino" target="_blank" rel="noopener noreferrer">
        </a>
        <a href="https://x.com/hanabananaxx_?s=21" target="_blank" rel="noopener noreferrer">
        </a>
      </div>
    </div>
  </footer>
</template>

<script>
export default {
  name: "FooTer",
};
</script>

<style scoped>
.footer {
  background-color: #f3e8ff; /* Light purple background */
  border: 3px solid #a855f7; /* Bold purple border */
  border-radius: 16px; /* Rounded corners for a cute look */
  padding: 1.5rem;
  text-align: center;
  margin: 20px auto;
  width: 90%;
  max-width: 800px;
  font-family: "Poppins", sans-serif;
  box-shadow: 0 6px 12px rgba(0, 0, 0, 0.1);
}

.footer-content {
  display: flex;
  flex-direction: column;
  align-items: center;
}

.footer-text {
  font-size: 1rem;
  color: #6b21a8; /* Deep purple text */
  margin-bottom: 1rem;
}

.footer-social {
  display: flex;
  gap: 1.5rem;
}

.footer-social a {
  display: inline-block;
  transition: transform 0.3s;
}

.footer-social a:hover {
  transform: scale(1.2); /* Enlarge icons on hover */
}

.social-icon {
  width: 28px;
  height: 28px;
  transition: transform 0.3s;
}

.social-icon:hover {
  transform: scale(1.3);
  filter: drop-shadow(0px 0px 4px #a855f7); /* Cute glowing effect on hover */
}
</style>
