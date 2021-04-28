<template>

  <div class="q-pa-md">



    <div class="row">
      <div class="col-12 col-md-6">
           
        <div class="q-pa-md">
    <q-toolbar class="bg-primary text-white">
      <q-btn flat round dense icon="menu" class="q-mr-sm" />
      <q-avatar>
        <img src="https://cdn.quasar.dev/logo/svg/quasar-logo.svg">
      </q-avatar>

      <q-toolbar-title>Quasar Framework</q-toolbar-title>

      <q-btn flat round dense icon="whatshot" />
    </q-toolbar>
  </div>
           
           
      </div>
      
    <div class="col-12 col-md-6">
        <div class="q-pa-md">
          <div class="q-gutter-md">
            <q-carousel
              v-model="slide"
              transition-prev="scale"
              transition-next="scale"
              swipeable
              animated
              control-color="white"
              navigation
              padding
              arrows
              height="720px"
              class="carousel"

            >
          <!-- class="bg-red text-white shadow-1 rounded-borders" -->
              <q-carousel-slide name="style" class="column no-wrap flex-center">
                <q-img :src="wireframeImg" class="iconImg" alt="Pencil, Pen and Erasers Icon">
                  </q-img>
                  
              </q-carousel-slide>
                
                <q-carousel-slide name="tv" class="column no-wrap flex-center">
                  <q-img :src="image" class="iconImg" alt="Pencil, Pen and Erasers Icon">
                  </q-img>
                </q-carousel-slide>
        
              <q-carousel-slide name="layers" class="column no-wrap flex-center">
                <q-img :src="responsiveImg" class="iconImg" alt="Pencil, Pen and Erasers Icon">
                  </q-img>
              
              </q-carousel-slide>
        
            </q-carousel>

      
    </div>
  </div>
      </div>
    </div>

  </div>
</template>



<script>

import image from '../assets/slideimage.png';
import wireframeImg from '../assets/video.png';
import responsiveImg from '../assets/responsive-design.png';
// import image from '../assets/slideimage.png';
// import wireframeImg from '../assets/wireframe.png';
// import responsiveImg from '../assets/responsive-design.png';
export default {
  data() {
    return {
      slide: 'style',
      image: image,
      wireframeImg: wireframeImg,
      responsiveImg: responsiveImg,
      
            
    }
  }
}
</script>

<style lang="scss">

.carousel{
  background-color: #80C2FF;
  border-radius: 50px;
  width: 95%;
}

.iconImg{
  // height: 169.86px;
  // width: 213.73px;
  // margin-left: 4rem;
  display: block;
  margin-left: auto;
  margin-right: auto;
  width: 33%;
}

.aboutColumn1{
  float: left;
  width: 50%;
}

.aboutRow::after{
  content: "";
  display: table;
  clear: both;
}

</style>
