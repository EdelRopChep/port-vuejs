<template>
    <Header/>
    <div class="projects-container">
      <h1 class="title">My Projects</h1>
      <p class="subtitle">Here are some of the projects I've been working on as I learn to code:</p>
      
      <div class="projects-grid">
        <div v-for="(project, index) in projects" :key="index" class="project-card">
          <img :src="project.image" :alt="project.title" class="project-image">
          <div class="project-info">
            <h2>{{ project.title }}</h2>
            <p>{{ project.description }}</p>
            <div class="tech-stack">
              <span v-for="(tech, techIndex) in project.technologies" :key="techIndex" class="tech-tag">
                {{ tech }}
              </span>
            </div>
            <div class="project-links">
              <a v-if="project.github" :href="project.github" target="_blank" rel="noopener noreferrer">GitHub</a>
              <a v-if="project.demo" :href="project.demo" target="_blank" rel="noopener noreferrer">Live Demo</a>
            </div>
          </div>
        </div>
      </div>
    </div>
    <Footer/>
  </template>
  
  <script>
  import Header from '~/components/Header.vue';
  import Footer from '~/components/Footer.vue';
  export default {
    components: {
      Header,
      Footer
    },

    name: 'ProjectsPage',
    data() {
      return {
        projects: [
          {
            title: "Personal Portfolio Website",
            description: "A responsive website to showcase my projects and skills, built with Vue.js and Nuxt.",
            image: "#",
            technologies: ["Vue.js", "Nuxt.js", "HTML", "CSS"],
            github: "https://github.com/yourusername/portfolio",
            demo: "https://your-portfolio-url.com"
          },
          {
            title: "Weather App",
            description: "A simple weather application that fetches and displays current weather data for a given location.",
            image: "#",
            technologies: ["JavaScript", "API", "HTML", "CSS"],
            github: "https://github.com/yourusername/weather-app",
            demo: "https://your-weather-app-url.com"
          },
          {
            title: "To-Do List App",
            description: "A basic to-do list application with the ability to add, complete, and delete tasks.",
            image: "#",
            technologies: ["Vue.js", "LocalStorage", "HTML", "CSS"],
            github: "https://github.com/yourusername/todo-app"
          }
        ]
      }
    },
    head() {
      return {
        title: 'My Projects - Edel Chepkemboi',
        meta: [
          { hid: 'description', name: 'description', content: 'Explore the coding projects of Edel Chepkemboi, an aspiring web developer.' }
        ]
      }
    }
  }
  </script>
  
  <style scoped>
  .projects-container {
    max-width: 1200px;
    margin: 0 auto;
    padding: 2rem;
    font-family: Arial, sans-serif;
  }
  
  .title {
    text-align: center;
    color: #2c3e50;
    margin-bottom: 0.5rem;
  }
  
  .subtitle {
    text-align: center;
    color: #7f8c8d;
    margin-bottom: 2rem;
  }
  
  .projects-grid {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
    gap: 2rem;
  }
  
  .project-card {
    background-color: #ffffff;
    border-radius: 10px;
    overflow: hidden;
    box-shadow: 0 4px 6px rgba(0, 0, 0, 0.1);
    transition: transform 0.3s ease;
  }
  
  .project-card:hover {
    transform: translateY(-5px);
  }
  
  .project-image {
    width: 100%;
    height: 200px;
    object-fit: cover;
  }
  
  .project-info {
    padding: 1.5rem;
  }
  
  .project-info h2 {
    color: #2c3e50;
    margin-bottom: 0.5rem;
  }
  
  .project-info p {
    color: #34495e;
    margin-bottom: 1rem;
  }
  
  .tech-stack {
    display: flex;
    flex-wrap: wrap;
    gap: 0.5rem;
    margin-bottom: 1rem;
  }
  
  .tech-tag {
    background-color: #3498db;
    color: white;
    padding: 0.25rem 0.5rem;
    border-radius: 15px;
    font-size: 0.8rem;
  }
  
  .project-links {
    display: flex;
    gap: 1rem;
  }
  
  .project-links a {
    text-decoration: none;
    color: #3498db;
    font-weight: bold;
    transition: color 0.3s ease;
  }
  
  .project-links a:hover {
    color: #2980b9;
  }
  </style>