

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
            <img v-if="carouselCounter === 0" :src= item.imgOne alt="">
            <img v-else-if="carouselCounter === 1" :src= item.imgTwo alt="">
            <div class="featured-card-text">
              <h3>{{ item.title }}</h3>
              <p>{{ item.subtitle }}</p>
            </div>
           
         </div>
         
        </div>
      </div>
      <div>
        <button @click="prevItem">prev</button>
        <button @click="nextItem">next</button>
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
        {imgOne: questLog,imgTwo: syncUp,title: 'Quest Log', subtitle: 'UX'},
     
      ],
      
    }
  },
  methods: {
    prevItem(){
      this.carouselCounter--
      if(this.carouselCounter < 0){
        this.carouselCounter = 1
      }
      console.log(this.carouselCounter);
    },
    nextItem(){
      this.carouselCounter++
      if(this.carouselCounter > 1){
        this.carouselCounter = 0
      }
      console.log(this.carouselCounter);

    }
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
      box-shadow:black 2px 8px 12px;
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
