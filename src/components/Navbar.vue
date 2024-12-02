<template>
    <nav class="navbar">
      <h1>🏡 Maju Jaya</h1>
      <ul>
        <li><a href="#home">Home</a></li>
        <li><a href="#features">Fitur</a></li>
        <li><a href="#gallery">Galeri</a></li>
        <li><a href="#contact">Kontak</a></li>
      </ul>
    </nav>
  </template>
  
  <style lang="scss">
  .navbar {
    display: flex;
    justify-content: space-between;
    align-items: center;
    padding: 1rem 2rem;
    background-color: #ffffff;
    box-shadow: 0 2px 5px rgba(0, 0, 0, 0.1);
  
    ul {
      display: flex;
      list-style: none;
  
      li {
        margin: 0 1rem;
        a {
          text-decoration: none;
          color: #333;
          transition: color 0.3s;
          &:hover {
            color: #4caf50;
          }
        }
      }
    }
  }
  </style>
  