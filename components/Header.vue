<template>
    <header class="header">
      <div class="logo">
        <img src="~/assets/logo.png" alt="Logo" />
      </div>
      <nav class="nav">
        <ul>
          <li><a href="/">Home</a></li>
          <li><a href="/about">About</a></li>
          <li><a href="/project">Projects</a></li>
          <li><a href="/contact">Contact</a></li>
        </ul>
      </nav>
    </header>
  </template>
  
  <script>
  export default {
    name: 'Header'
  }
  </script>
  
  <style scoped>
  .header {
    display: flex;
    justify-content: space-between;
    align-items: center;
    padding: 1rem 2rem;
    background-color:aqua
  }
  
  .logo img {
    height: 50px;
    width: 50px;
  }
  
  .nav ul {
    display: flex;
    list-style-type: none;
    margin: 0;
    padding: 0;
  }
  
  .nav li {
    margin-left: 1rem;
  }
  
  .nav a {
    text-decoration: none;
    color: #333;
    font-weight: bold;
  }
  </style>