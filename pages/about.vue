<template>
    <Header/>
    <div class="about-container">
      <h1 class="title">About Me</h1>
      <div class="content">
        <div class="profile-section">
          <div class="image-container">
            <img src="~/assets/profile.jpg" alt="Edel Chepkemboi's profile picture">
          </div>
          <h2>Edel Chepkemboi</h2>
          <p class="tagline">Aspiring Web Developer | Lifelong Learner</p>
        </div>
        <div class="info-section">
          <h3>My Journey</h3>
          <p>
            Hello! I'm Edel, a passionate beginner programmer on an exciting journey into the world of web development. 
            My fascination with technology and problem-solving led me to dive into coding, and I've been hooked ever since.
          </p>
          <h3>What I'm Learning</h3>
          <ul class="skills-list">
            <li>HTML5 & CSS3</li>
            <li>JavaScript</li>
            <li>Vue.js & Nuxt.js</li>
            <li>Responsive Web Design</li>
            <li>Version Control with Git</li>
          </ul>
          <h3>My Goals</h3>
          <p>
            As I continue to grow my skills, I aim to build intuitive and user-friendly web applications. 
            I'm excited about the endless possibilities in tech and look forward to contributing to innovative projects.
          </p>
          <h3>Let's Connect!</h3>
          <p>
            I'm always eager to learn and collaborate. Feel free to reach out if you'd like to connect, 
            share knowledge, or work on a project together.
          </p>
          <div class="social-links">
            <a href="https://github.com/edel-chepkemboi" target="_blank" rel="noopener noreferrer">GitHub</a>
            <a href="https://www.linkedin.com/in/edel-chepkemboi" target="_blank" rel="noopener noreferrer">LinkedIn</a>
          </div>
        </div>
      </div>
    </div>
    <Footer/>
  </template>
  
  <script>
  import Header from '~/components/Header.vue'
  import Footer from '~/components/Footer.vue'
  
  export default {
    components: {
      Header,
      Footer
    },
    name: 'AboutPage',
    head() {
      return {
        title: 'About Edel Chepkemboi - Aspiring Web Developer',
        meta: [
          { hid: 'description', name: 'description', content: 'Learn about Edel Chepkemboi, an aspiring web developer and her journey in programming.' }
        ]
      }
    }
  }
  </script>
  
  <style scoped>
  .about-container {
    max-width: 800px;
    margin: 0 auto;
    padding: 2rem;
    font-family: Arial, sans-serif;
    color: #333;
    background-color:aqua;
    border-radius: 10px;
    box-shadow: 0 0 10px rgba(0,0,0,0.1);
    
  }
  
  .title {
    text-align: center;
    color: #2c3e50;
    margin-bottom: 2rem;
  }
  
  .content {
    display: flex;
    flex-direction: column;
    gap: 2rem;
  }
  
  .profile-section {
    text-align: center;
  }
  
  .image-container {
    width: 200px;
    height: 200px;
    margin: 0 auto 1rem;
    border-radius: 50%;
    overflow: hidden;
    border: 3px solid #3498db;
  }
  
  .image-container img {
    width: 100%;
    height: 100%;
    object-fit: cover;
  }
  
  .tagline {
    font-style: italic;
    color: #7f8c8d;
  }
  
  .info-section h3 {
    color: #2980b9;
    margin-top: 1.5rem;
  }
  
  .skills-list {
    display: flex;
    flex-wrap: wrap;
    gap: 0.5rem;
    padding: 0;
  }
  
  .skills-list li {
    list-style: none;
    background-color: #3498db;
    color: white;
    padding: 0.5rem 1rem;
    border-radius: 20px;
    font-size: 0.9rem;
  }
  
  .social-links {
    display: flex;
    justify-content: center;
    gap: 1rem;
    margin-top: 1rem;
  }
  
  .social-links a {
    text-decoration: none;
    color: #3498db;
    font-weight: bold;
    transition: color 0.3s ease;
  }
  
  .social-links a:hover {
    color: #2c3e50;
  }
  
  @media (min-width: 768px) {
    .content {
      flex-direction: row;
    }
    
    .profile-section {
      flex: 1;
    }
    
    .info-section {
      flex: 2;
    }
  }
  </style>