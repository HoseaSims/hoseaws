<template>
  <div class="home">
    <div id="top-img">
      <img src="../assets/frame.png" alt="">
    </div>
    <div id="featured-container">
      <p>Featured Projects</p>
      <div class="featured-card">
        <img src="../assets/frame.png" alt="">
        <div class="featured-card-text">
          <h4>This is the title</h4>
          <p>UX</p>
        </div>
      </div>
    </div>
    <div>
      <p>about</p>
      <img src="../assets/sampleimg.png" alt="">
    </div>
  </div>
</template>

<script>
// @ is an alias to /src

</script>

<style>
.home{
  
}

#top-img{
  margin-bottom: 24px;
}
#featured-container{
 margin-left: 12px; 
 box-shadow:black 2px 8px 12px;
}
.featured-card-text{
  background: rgb(33,51,71);
  background: linear-gradient(0deg, rgba(33,51,71,1) 20%, rgba(13,21,29,1) 78%);
}
.featured-card-text h4{
  font-size: 24px;
  margin: 0;
  padding: 8px 0 0 8px;
}
.featured-card-text p{
  margin: 0;
  padding: 0 0 18px 8px;
  color: #C8ED4E;
}
</style>
