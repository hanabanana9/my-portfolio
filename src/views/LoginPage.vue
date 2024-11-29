<template>
  <div class="login-container">
    <div class="login-box">
      <h2>Login</h2>
      <form @submit.prevent="login" class="login-form">
        <input 
          v-model="username" 
          placeholder="Username" 
          class="input-field" 
        />
        <input 
          v-model="password" 
          type="password" 
          placeholder="Password" 
          class="input-field" 
        />
        <button type="submit" class="login-button">Login</button>
      </form>
      <p v-if="error" class="error-message">{{ error }}</p>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      username: '',
      password: '',
      error: ''
    };
  },
  methods: {
    login() {
      if (this.username === 'hannah.cancino' && this.password === 'Namwoohyun1991!') {
        this.$router.push('/portfolio/profile');
      } else {
        this.error = 'Invalid login credentials';
      }
    }
  }
};
</script>

<style scoped>
@import url('https://fonts.googleapis.com/css2?family=Poppins:wght@400;600&display=swap');

body {
  margin: 0;
  font-family: 'Poppins', sans-serif;
  background-color: #f4f4f9;
}

.login-container {
  display: flex;
  align-items: center;
  justify-content: center;
  height: 100vh;
  background-color: #7b4da9;
}

.login-box {
  background-color: #ffffff;
  padding: 2rem;
  border-radius: 12px;
  box-shadow: 0 8px 20px rgba(0, 0, 0, 0.2);
  text-align: center;
  max-width: 400px;
  width: 100%;
}

h2 {
  font-size: 2rem;
  margin-bottom: 1.5rem;
  color: #7b4da9;
  font-weight: 600;
}

.login-form {
  display: flex;
  flex-direction: column;
}

.input-field {
  margin-bottom: 1rem;
  padding: 1rem;
  border: 1px solid #e0e0e0;
  border-radius: 8px;
  font-size: 1rem;
  background-color: #f9f9fc;
  color: #333;
  transition: all 0.3s ease;
}

.input-field:focus {
  border-color: #7b4da9;
  box-shadow: 0 0 5px rgba(123, 77, 169, 0.5);
  outline: none;
}

.login-button {
  padding: 0.75rem;
  background-color: #7b4da9;
  color: white;
  border: none;
  border-radius: 8px;
  font-size: 1rem;
  font-weight: 600;
  cursor: pointer;
  transition: background-color 0.3s ease;
}

.login-button:hover {
  background-color: #8e61b3;
}

.error-message {
  margin-top: 1rem;
  color: #e74c3c;
  font-size: 0.9rem;
  background-color: #f8d7da;
  padding: 0.5rem;
  border-radius: 5px;
}
</style>
