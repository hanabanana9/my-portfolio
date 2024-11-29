<template>
  <div class="contact-page">
    <h2>Contact Me</h2>
    <form @submit.prevent="submitForm" class="contact-form">
      <input
        v-model="form.name"
        placeholder="Name"
        required
        class="form-input"
      />
      <input
        v-model="form.email"
        type="email"
        placeholder="Email"
        required
        class="form-input"
      />
      <textarea
        v-model="form.message"
        placeholder="Message"
        required
        class="form-textarea"
      ></textarea>
      <button type="submit" class="form-button">Send Message</button>
    </form>
    <p v-if="submitted" class="thank-you-message">
      Thanks for reaching out! I'll get back to you soon.
    </p>
  </div>
</template>

<script>
export default {
  data() {
    return {
      form: {
        name: '',
        email: '',
        message: ''
      },
      submitted: false
    };
  },
  methods: {
    submitForm() {
      if (this.form.name && this.form.email && this.form.message) {
        this.submitted = true;
        console.log('Form Submitted', this.form);
        this.form = { name: '', email: '', message: '' };
      }
    }
  }
};
</script>

<style scoped>
@import url('https://fonts.googleapis.com/css2?family=Poppins:wght@400;600&display=swap');

.contact-page {
  max-width: 750px;
  margin: 0 auto;
  padding: 40px;
  text-align: center;
  background-color: #7b4da9;
  border-radius: 15px;
  box-shadow: 0 8px 16px rgba(0, 0, 0, 0.2);
}

h2 {
  font-family: 'Poppins', sans-serif;
  font-size: 32px;
  color: #ffffff;
  margin-bottom: 30px;
}

.contact-form {
  display: flex;
  flex-direction: column;
}

.form-input,
.form-textarea {
  width: 100%;
  padding: 20px;
  margin: 15px 0;
  border-radius: 10px;
  border: 1px solid #e6d6f3;
  font-size: 18px;
  font-family: 'Poppins', sans-serif;
  background-color: #ffffff;
  color: #5a2c88;
}

.form-textarea {
  height: 150px;
  resize: vertical;
}

.form-button {
  padding: 15px 30px;
  margin-top: 20px;
  background-color: #5a2c88;
  border: none;
  border-radius: 10px;
  color: white;
  font-size: 18px;
  font-family: 'Poppins', sans-serif;
  cursor: pointer;
  transition: background-color 0.3s ease;
}

.form-button:hover {
  background-color: #8b5fbf;
}

.thank-you-message {
  margin-top: 30px;
  color: #ffffff;
  font-size: 20px;
  font-family: 'Poppins', sans-serif;
}
</style>
