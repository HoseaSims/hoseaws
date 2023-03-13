<template>
  <div>
    <head>
      <link rel="preconnect" href="https://fonts.googleapis.com">
      <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
      <link href="https://fonts.googleapis.com/css2?family=Roboto&family=Unbounded&display=swap" rel="stylesheet">
    </head>
    <nav>
      <img id="logo-img" src="./assets/logo.png" alt="">
      <router-link to="/">Projects</router-link> 
      <router-link to="/about">About</router-link>
      <router-link to="/contact">contact</router-link>
    </nav>
    <router-view/>
  </div>
</template>

<style>
@media only screen and (max-width: 910px)  {
  
  body{
    color: white;
    height: 100vh;
    margin: 0;
    padding: 0;
    background-color: #283D58;
    font-family: 'Roboto', sans-serif;
    /* font-family: 'Unbounded', cursive; */
  }
  nav{
    text-align: center;
    background-color: #1F2126;
    display: flex;
    justify-content: space-around;
    align-items: center;
  }
  nav a{
  text-decoration: none;
  color: white;
  font-size: 16px;
  padding-left: 16px;
  align-content: center;
  
}
#logo-img{
  width: 40px;
}
}

</style>
