

<template>
  <div class="home">
    <div id="top-img">
      <img src="../assets/frame.png" alt="">
    </div>
    <div id="main-container">
      <p>Featured Projects</p>
      <div id="featured-container">
        <div class="featured-card" v-for="(item, index) in items" :key="index">
         <div>
            <img :src= item.img alt="">
            <div class="featured-card-text">
              <h3>{{ item.title }}</h3>
              <p>{{ item.subtitle }}</p>
            </div>
           
         </div>
         
        </div>
      </div>
      <div id="about-sample">
        <p>about</p>
        <img src="../assets/sampleimg.png" alt="">
      </div>
    </div>
  </div>
</template>

<script>
// @ is an alias to /src
import questLog from '../assets/QuestLogImg.png'
import syncUp from '../assets/SyncUp.png'
export default{
  data(){
    return{
      questlogTitle: 'Quest Log',
      uxSub: 'UX',
      webDev: 'Web Development',
      carouselCounter: 0,

      items: [
        {img: questLog, title: 'Quest Log', subtitle: 'UX'},
        {img: syncUp, title: 'Sync Up', subtitle: 'UX'}
      ],
      
    }
  },
  methods: {

  }
}
</script>

<style>

@media only screen and (max-width: 910px){

    .home{
      
    }
    #main-container{
      margin: 0 12px 0 12px;
    }
    #top-img{
      margin-bottom: 24px;
      width: auto;
    }
    #top-img img{
      width: 100%;
    }
    #featured-container{
      width: 400px;
      display: flex;
      width: 100%;
      overflow-x: scroll;
      white-space: nowrap;
      
      scroll-snap-type: x always;
      scroll-snap-align: start;
    }
    .featured-card{
      margin-right: 16px;
      scroll-snap-stop: always;
  }
  .featured-card img{
    width: 400px;
  }
  .featured-card-text{
    background: rgb(33,51,71);
    background: linear-gradient(0deg, rgba(33,51,71,1) 20%, rgba(13,21,29,1) 78%);
  }
  .featured-card-text h3{
    font-size: 24px;
    margin: 0;
    padding: 8px 0 0 8px;
  }
  .featured-card-text p{
    margin: 0;
    padding: 0 0 18px 8px;
    color: #C8ED4E;
  }
  #about-sample{

  }
  #about-sample img{
    width: 400px;
  }
}
</style>
