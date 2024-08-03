<template>
    <div>
      <Header/>
      <div class="container">
        <div class="image-side">
          <img src="~/assets/pro.jpeg" alt="Edel Chepkemboi's profile picture">
        </div>
        <div class="content-side">
          <h1>Hello,</h1>
          <p>I am Edel Chepkemboi.</p>
          <p>I'm into web and software development</p>
          <div class="social-links">
            <a href="https://www.linkedin.com/in/edel-chepkemboi" target="_blank" rel="noopener noreferrer">
              LinkedIn
            </a>
            <a href="https://github.com/edel-chepkemboi" target="_blank" rel="noopener noreferrer">
              GitHub
            </a>
          </div>
        </div>
      </div>
      <Footer/>
    </div>
  </template>
  
  <script>
  import Header from '~/components/Header.vue'
  import Footer from '~/components/Footer.vue'
  
  export default {
    components: {
      Header,
      Footer
    },
    name: 'IndexPage',
    head() {
      return {
        title: 'Edel Chepkemboi - Web and Software Developer',
        meta: [
          { hid: 'description', name: 'description', content: 'Personal website of Edel Chepkemboi, a web and software developer.' }
        ]
      }
    }
  }
  </script>
  
  <style scoped>
  .container {
    display: flex;
    min-height: 100vh;
    background-color: aq
  }
  
  .image-side, .content-side {
    flex: 1;
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
    padding: 20px;
  }
  
  .image-side img {
    max-width: 100%;
    height: auto;
  }
  
  .content-side {
    text-align: center;
  }
  
  .social-links {
    margin-top: 20px;
  }
  
  .social-links a {
    margin: 0 10px;
    text-decoration: none;
    color: #333;
    font-weight: bold;
  }
  
  @media (max-width: 768px) {
    .container {
      flex-direction: column;
    }
  }
  </style>