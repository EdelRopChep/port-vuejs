<template>
    <footer class="footer">
      <p>&copy; {{ currentYear }} Chepkemboi. All rights reserved.</p>
      <button @click="scrollToTop" class="scroll-top">↑</button>
    </footer>
  </template>
  
  <script>
  export default {
    name: 'Footer',
    computed: {
      currentYear() {
        return new Date().getFullYear()
      }
    },
    methods: {
      scrollToTop() {
        window.scrollTo({
          top: 0,
          behavior: 'smooth'
        })
      }
    }
  }
  </script>
  
  <style scoped>
  .footer {
    display: flex;
    justify-content: center;
    align-items: center;
    padding: 1rem 2rem;
    background-color:aqua;
    position: relative;
  }
  
  .scroll-top {
    background-color: #de14c9;
    color: white;
    border: none;
    border-radius: 50%;
    width: 40px;
    height: 40px;
    font-size: 20px;
    cursor: pointer;
    transition: background-color 0.3s;
  }
  
  .scroll-top:hover {
    background-color: #555;
  }
  </style>