<template>
  <div id="app">
    <div class="card">
      <form @submit.prevent="submitForm">
        <div class="form-group">
          <label for="name">Name:</label>
          <input type="text" id="name" v-model="formData.name">
        </div>

        <div class="form-group">
          <label for="email">Email:</label>
          <input type="email" id="email" v-model="formData.email">
        </div>

        <div class="form-group">
          <label for="phone">Phone:</label>
          <input type="tel" id="phone" v-model="formData.phone">
        </div>

        <div class="form-group">
          <label for="message">Message:</label>
          <textarea id="message" v-model="formData.message" rows="6"></textarea>
        </div>

        <button type="submit">Submit</button>
      </form>
    </div>
  </div>
</template>

<script>
import { reactive } from 'vue';

export default {
  setup() {
    const formData = reactive({
      name: '',
      email: '',
      phone: '',
      message: ''
    });

    const submitForm = () => {
      console.log('Form submitted');
      console.log(formData);
    };

    return {
      formData,
      submitForm
    };
  }
};
</script>

<style>
#app {
  display: flex;
  justify-content: center;
  align-items: center;
  height: 100vh;
}

.card {
  background-color: #fff;
  border-radius: 8px;
  box-shadow: 0px 4px 8px rgba(0, 0, 0, 0.1);
  padding: 20px;
  width: 400px;
}

.form-group {
  margin-bottom: 20px;
  text-align: left;
}

label {
  display: block;
  margin-bottom: 5px;
  font-weight: bold;
}

input[type="text"],
input[type="email"],
input[type="tel"],
textarea {
  width: 100%;
  padding: 10px;
  margin-top: 5px;
  border: 1px solid #ccc;
  border-radius: 4px;
  box-sizing: border-box;
}

button {
  background-color: #4CAF50;
  color: white;
  padding: 12px 24px;
  border: none;
  border-radius: 4px;
  cursor: pointer;
  font-size: 16px;
}

button:hover {
  background-color: #45a049;
}
</style>
