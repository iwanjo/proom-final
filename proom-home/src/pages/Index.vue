<template>
  <div class="q-pa-md">

    <div class="row">
      <div class="col">
           
           
      </div>
      
    <div class="col">
      <template>
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
                <q-icon name="style" size="56px" />
                  
              </q-carousel-slide>
                
                <q-carousel-slide name="tv" class="column no-wrap flex-center">
                  <q-img :src="image" class="iconImg">
                  </q-img>
                </q-carousel-slide>
        
              <q-carousel-slide name="layers" class="column no-wrap flex-center">
                <q-icon name="layers" size="56px" />
              
              </q-carousel-slide>
        
      </q-carousel>

      
    </div>
  </div>
</template>
      </div>
    </div>

  </div>
</template>



<script>
import image from '../assets/slideimage.png'
export default {
  data() {
    return {
      slide: 'style',
      lorem: 'Lorem Ipsum asdasdas',
      image: image
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
  height: 169.86px;
  width: 213.73px;
  
  
  
}

</style>