<template>
  <div id="app-container">
    <nav>
      <router-link to="/"><img id="logo-img" src="./assets/logo.png" alt=""></router-link>
      <router-link to="/about">About</router-link>
      <router-link to="/contact">Contact</router-link>
      <router-link to="/projects">Projects</router-link>
    </nav>
    <router-view/>
  </div>
</template>

<style>
@media only screen and (max-width: 910px)  {
  html{
    overflow-x: hidden;
    max-width: 100%;
  }
  body{
    max-width: 100%;
    color: white;
    height: 100vh;
    margin: 0;
    padding: 0;
    background-color: #283D58;
    font-family: 'Roboto', sans-serif;
    overflow-x: hidden;
    /* font-family: 'Unbounded', cursive; */
  }
  #app-container{

  }
  nav{
    text-align: center;
    background-color: #1F2126;
    display: flex;
    justify-content: space-around;
    align-items: center;
    /* width: 100%; */
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
