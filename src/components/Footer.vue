<template>
    <footer class="footer">
      <p class="footer-text">made with <i class="heart-icon"></i> by Marco</p>
    </footer>
  </template>
  
  <style scoped>
  .footer {
    position: fixed;
    z-index:10;
    margin-top:3rem;
    bottom: 0;
    left: 0;
    width: 100%;
    background-color: #03001C; 
    padding: 1rem;
    text-align: center;
  }
  
  .footer-text {
    margin: 0;
    font-size: 0.8rem;
    color:aquamarine;
  }
  
  .heart-icon {
    display: inline-block;
    width: 20px;
    height: 20px;
    background-color: red;
    clip-path: polygon(
      50% 15%,
      61% 6%,
      78% 36%,
      50% 90%,
      22% 36%,
      39% 6%
    );
    margin-left: 0.3rem;
  }
  </style>
  