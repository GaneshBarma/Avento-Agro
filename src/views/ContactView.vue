<template>
  <div class="contact">
    <h1>Contact Us</h1>
    <p>Get in touch with our team.</p>
    <form @submit.prevent="submitForm" class="contact-form">
      <div class="form-row">
        <div class="form-group">
          <input v-model="form.name" type="text" placeholder="Name" required />
        </div>
        <div class="form-group">
          <input v-model="form.email" type="email" placeholder="Email" required />
        </div>
      </div>
      <div class="form-row">
        <div class="form-group">
          <input v-model="form.phone" type="tel" placeholder="Phone Number" required />
        </div>
        <div class="form-group">
          <input v-model="form.company" type="text" placeholder="Company (optional)" />
        </div>
      </div>
      <div class="form-row">
        <div class="form-group full-width">
          <input v-model="form.title" type="text" placeholder="Title" required />
        </div>
      </div>
      <div class="form-group full-width">
        <textarea v-model="form.message" placeholder="Message" required></textarea>
      </div>
      <button type="submit">Submit</button>
    </form>
  </div>
</template>

<script lang="ts" setup>
import { ref } from 'vue';

const form = ref({
  name: '',
  email: '',
  phone: '',
  company: '',
  title: '',
  message: '',
});

const submitForm = () => {
  if (form.value.name && form.value.email && form.value.phone && form.value.title && form.value.message) {
    alert('Form submitted successfully!');
    // Handle the form submission, e.g., send the data to a server.
    form.value.name = '';
    form.value.email = '';
    form.value.phone = '';
    form.value.company = '';
    form.value.title = '';
    form.value.message = '';
  } else {
    alert('Please fill out all required fields.');
  }
};
</script>

<style scoped>
.contact {
  text-align: center;
  margin-top: 2rem;
  display: flex;
  flex-direction: column;
  align-items: center;
}

.contact p {
  margin-bottom: 2rem; /* Added margin-bottom for spacing */
}

.contact-form {
  display: flex;
  flex-direction: column;
  align-items: center;
  width: 100%;
  max-width: 600px;
}

.form-row {
  display: flex;
  justify-content: space-between;
  width: 100%;
  margin-bottom: 1rem;
}

.form-group {
  flex: 1;
  margin-right: 1rem;
}

.form-group:last-child {
  margin-right: 0;
}

.form-group.full-width {
  width: 100%;
  margin-right: 0;
}

.form-group input,
.form-group textarea {
  width: 100%;
  padding: 0.75rem;
  border: 1px solid var(--color-border);
  border-radius: 4px;
  font-size: 1rem;
  box-sizing: border-box;
  font-family: 'Montserrat', sans-serif; /* Ensure Montserrat font for inputs and textareas */
}

.form-group input::placeholder,
.form-group textarea::placeholder {
  font-family: 'Montserrat', sans-serif; /* Ensure Montserrat font for placeholders */
}

textarea {
  height: 100px;
}

button {
  padding: 0.75rem 1.5rem;
  font-size: 1rem;
  color: var(--color-background);
  background-color: orange;
  border: none;
  border-radius: 4px;
  cursor: pointer;
  transition: background-color 0.3s ease;
  margin-top: 1rem;
  font-family: 'Montserrat', sans-serif; /* Ensure Montserrat font for button */
  font-weight: bold; /* Bold weight for button */
}

button:hover {
  background-color: darkorange;
}
</style>
