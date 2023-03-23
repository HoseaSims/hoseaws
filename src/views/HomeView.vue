

<template>
  <div class="home">
    <div id="top-img">
      <img src="../assets/frame.png" alt="">
    </div>
    <div id="main-container">
      <p>Featured Projects</p>
      <div id="featured-container">
        <div class="featured-card">
          <img src="{{ test }}" alt="">
          <div class="featured-card-text">
            <h4> {{ questlogTitle }}</h4>
            <p>{{ uxSub }}</p>
          </div>
        </div>
      </div>
      <div id="about-sample">
        <p>about</p>
        <img src="../assets/sampleimg.png" alt="">
      </div>
    </div>

    <div :index="activeItem">
      <div v-for="(item, index) in items" :key="index">
        <div>
          <img :src= this.test alt="">
          <h3>{{ item.title }}</h3>
          <p>{{ item.subtitle }}</p>
          <p></p>
        </div>
       
      </div>
    </div>
  <div>
    <button @click="prevItem">prev</button>
    <button @click="nextItem">next</button>
  </div>

  </div>
</template>

<script>
// @ is an alias to /src

export default{
  data(){
    return{
      test: '../assets/QuestLogImg.png',
      questlogTitle: 'Quest Log',
      uxSub: 'UX',
      webDev: 'Web Development',

      items: [
        {src: "../assets/logo.png", title: 'This is a title :)', subtitle: 'this is a subtitle'},
        {otherTitle: 'WOO WOO WOO WOO'}
      ],
      activeItem: 0,
    }
  },
  methods: {
    prevItem(){
      this.activeItem = Math.max(this.activeItem -1,0)
      console.log('click prevItem');
      console.log(this.activeItem);
    },
    nextItem(){
      this.activeItem = Math.min(this.activeItem + 1, this.items.length - 1)
      console.log('clicked nextItem');
      console.log(this.items[0]);
      console.log(this.activeItem);

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
  #about-sample{

  }
  #about-sample img{
    width: 400px;
  }
}
</style>
