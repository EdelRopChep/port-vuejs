<!-- pages/contact.vue -->
<template>
    <div class="contact-page">
      <Header/>
      <h1>Contact Us</h1>
      
      <div class="contact-content">
        <div class="contact-form-container">
          <h2>Send us a message</h2>
          <form @submit.prevent="submitForm" class="contact-form">
            <div class="form-group">
              <label for="name">Name:</label>
              <input v-model="form.name" type="text" id="name" required>
            </div>
            
            <div class="form-group">
              <label for="email">Email:</label>
              <input v-model="form.email" type="email" id="email" required>
            </div>
            
            <div class="form-group">
              <label for="subject">Subject:</label>
              <input v-model="form.subject" type="text" id="subject" required>
            </div>
            
            <div class="form-group">
              <label for="message">Message:</label>
              <textarea v-model="form.message" id="message" rows="5" required></textarea>
            </div>
            
            <button type="submit">Send Message</button>
          </form>
        </div>
        
        <div class="contact-info">
          <h2>Contact Information</h2>
          <p><strong>Address:</strong> 123 Pharmacy Street, Healthville, MED 12345</p>
          <p><strong>Phone:</strong> (555) 123-4567</p>
          <p><strong>Email:</strong> info@yourdrugstore.com</p>
          <p><strong>Hours:</strong> Monday - Friday: 9am - 7pm<br>Saturday: 10am - 5pm<br>Sunday: Closed</p>
          
         <!-- <div class="map-placeholder"> -->
            <!-- Replace this with an actual map component or embed when available -->
           <!-- <img src="~/assets/map.jpeg" alt="Map" class="map-image"> -->
        <!-- </div> -->
        </div>
      </div>
    </div>
    <Footer/>
  </template>
  
  <script>
  import Header from '~/components/Header.vue';
  import Footer from '~/components/Footer.vue';
  export default {
    components:{
        Header,
        Footer
    },
    name: 'ContactPage',
    data() {
      return {
        form: {
          name: '',
          email: '',
          subject: '',
          message: ''
        }
      };
    },
    methods: {
      submitForm() {
        console.log('Form submitted:', this.form);
        // Here you would typically send this data to your backend
        // For now, we'll just log it and reset the form
        this.resetForm();
        alert('Thank you for your message. We will get back to you soon!');
      },
      resetForm() {
        this.form = {
          name: '',
          email: '',
          subject: '',
          message: ''
        };
      }
    }
  };
  </script>
  
  <style scoped>
  .contact-page {
    max-width: 1200px;
    margin: 0 auto;
    padding: 2rem;
  }
  
  h1 {
    text-align: center;
    margin-bottom: 2rem;
    font-weight: bolder;
    font-family: Verdana, Geneva, Tahoma, sans-serif;
  }
  
  .contact-content {
    display: flex;
    gap: 2rem;
  }
  
  .contact-form-container,
  .contact-info {
    flex: 1;
  }
  
  .contact-form {
    display: flex;
    flex-direction: column;
  }
  
  .form-group {
    margin-bottom: 1rem;
  }
  
  label {
    display: block;
    margin-bottom: 0.5rem;
  }
  
  input,
  textarea {
    width: 100%;
    padding: 0.5rem;
    border: 1px solid #ccc;
    border-radius: 4px;
  }
  
  button {
    padding: 0.5rem 1rem;
    background-color: #007bff;
    color: white;
    border: none;
    border-radius: 4px;
    cursor: pointer;
    transition: background-color 0.3s ease;
  }
  
  button:hover {
    background-color: #0056b3;
  }
  
  .map-placeholder {
    margin-top: 1rem;
    border: 1px solid #ccc;
    border-radius: 4px;
    overflow: hidden;
  }
  
  .map-image {
    width: 100%;
    height: auto;
    display: block;
  }
  
  @media (max-width: 768px) {
    .contact-content {
      flex-direction: column;
    }
  }
  </style>