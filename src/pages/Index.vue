
<template>

  <div class="q-pa-md">
    <div class="row">
      <!-- We are going to use responsive quasar grid layouts to help in resizing each layer according to specific breakpoints. -->
      <div class="col-12 col-md-6">
           
        <div class="q-pa-md">
    <q-toolbar class="text-black">
      <q-avatar>
        <q-img :src="ellipse" class="ellipseImg" alt="Logo Img">
        </q-img>
                
      </q-avatar>
      
      <!-- Here we will include the navbar. We will have the ellipse icon, brand name, and navigation links our users can access. On the far right will be a mail notifications icon and a profile picture. Picture obtained from Pexels. -->
      <q-toolbar-title class="title">Proom</q-toolbar-title>
      
        <ul class="nav-links">
            <li><a>Courses</a></li>
            <li><a>Features</a></li>
            <li><a>Support</a></li>

        </ul>

        <q-img :src="messageImg" class="messageImg" alt="Message Img">
        </q-img>
        <q-img :src="userImg" class="userImg" alt="Message Img">
        </q-img>

      </q-toolbar>
      </div>

      <!-- Here will be our main Call to action area. We will include our hook text, simple process and CTA button. -->

      <div class="cta-section">
        <h1 class="action-title">Study different areas of web design easily in 3 steps:</h1>
        <p class="steps-text"><span class="steps">.01</span>Visit our website</p>
        <p class="steps-text"><span class="steps">.02</span>Sign up</p>
        <p class="steps-text"><span class="steps">.03</span>Find the course you want</p>
        <button class="cta-button">Sign In</button>

      </div>

           
           
      </div>

      <!-- Below we are using a carousel provided by Quasar's documentation. I have modified it to have the same color as that in the Figma file, as well as included two more icons related to web design, to complete the look and feel of the product. -->
      <!-- The carousel will also utilize arrows as an additional navigation component that will be helpful for first-time and general users. -->

      
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
// Importing the necessary assets - images.

import image from '../assets/slideimage.png';
import wireframeImg from '../assets/video.png';
import responsiveImg from '../assets/responsive-design.png';
import ellipse from '../assets/ellipse.png';
import messageImg from '../assets/Messege.png';
import userImg from '../assets/user.jpeg';


export default {
  data() {
    return {
      model: 'one',
      slide: 'style',
      image: image,
      wireframeImg: wireframeImg,
      responsiveImg: responsiveImg,
      ellipse: ellipse,
      messageImg: messageImg,
      userImg: userImg
      
    }
  }
}
</script>




<style lang="scss">
// We will include our CSS here to be able to make changes more easily to our Quasar components. We will use the three fonts from the Figma prototype - Montserrat, Niramit and Mukta.

@import url('https://fonts.googleapis.com/css2?family=Montserrat&family=Mukta&family=Niramit&display=swap');
.title{
  font-family: 'Montserrat', sans-serif;
  margin-left: -.7rem;
  font-weight: bold;
  font-size: 18px;
  cursor: pointer;
}

.nav-links{
  list-style-type: none;
  // margin: 0;
  padding: 0;
  width: 70%;
  
}

.nav-links li{
  display: inline;
  padding: 1px 24px;
  font-family: 'Montserrat', sans-serif;
  font-size: 15.2px;
  color: #001A26;
  cursor: pointer;
  
}

.nav-links li:hover{
  color: #839EFF;
  
}

.messageImg{
  width: 24px;
  margin-top: -.3rem;

}

.userImg{
  width: 36px;
  border-radius: 50%;
  margin-left: .5rem;
}

.carousel{
  background-color: #80C2FF;
  border-radius: 50px;
  width: 95%;
}

.iconImg{
  // height: 169.86px; - Heights and width from the figma file.
  // width: 213.73px;
  display: block;
  margin-left: auto;
  margin-right: auto;
  width: 33%;
}

.ellipseImg{
  display: block;
  margin-left: auto;
  margin-right: auto;
  width: 12px;
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

.cta-section{
  padding: 3.5rem 0 2rem 9rem;
}


.action-title{
  font-family: 'Niramit', sans-serif;
  font-size: 45px;
  line-height: 4.5rem;
  font-weight: bold;
  width: 70%;
  padding-bottom: 1rem;
  
}

.steps{
  font-family: 'Mukta', sans-serif;
  color: #839EFF;
  font-weight: bold;
  margin-right: 1.4rem;
  font-size: 12px;
}

.steps-text{
  font-family: 'Montserrat', sans-serif;
  font-size: 18px;
}

.cta-button{
  margin-top: 2.4rem;
  background-color: #839EFF;
  padding: .7rem 2.5rem;
  color: white;
  font-family: 'Montserrat', sans-serif;
  font-size: 18px;
  font-weight: bold;
  outline: none;
  border: none;
  border-radius: 33px;
  cursor: pointer;
  box-shadow: 0 8px 16px 0 #C5D1FF;
}

.cta-button:hover{
  color: #839EFF;
  background-color: white;
  border: 1px solid #839EFF;
}

// Below we have included the responsive media queries and breakpoints for us to ensure this one pager web app looks pleasing on all screens, and allows the user to complete all their necessary functions.

@media screen and (max-width: 1362px) {
  .title{
    font-family: 'Montserrat', sans-serif;
    margin-left: -2.2rem;
    font-weight: bold;
    font-size: 15px;
    cursor: pointer;
  }
  .ellipseImg{
    display: block;
    margin-left: 0rem;
    width: 9.5px;
    
  }

  .nav-links{
    list-style-type: none;
    // margin: 0;
    padding: 0;
    width: 57%;
    
  }

  .nav-links li{
    display: inline;
    padding: 1px 10px;
    font-family: 'Montserrat', sans-serif;
    font-size: 13.5px;
    color: #001A26;
    cursor: pointer;
    
  }

  .action-title{
      font-family: 'Niramit', sans-serif;
      font-size: 34px;
      line-height: 3.5rem;
      font-weight: bold;
      width: 70%;
      padding-bottom: 1rem;
  }

  .cta-button{
    display: block;
    margin-left: auto;
    margin-right: auto;
    margin-top: 2.4rem;
    margin-bottom: 2rem;
    background-color: #839EFF;
    padding: .7rem 1.7rem;
    color: white;
    font-family: 'Montserrat', sans-serif;
    font-size: 15px;
    
  }
}

@media screen and (max-width: 1023px) {

  .cta-section{
    padding: 0rem;
    display: block;
    margin-left: auto;
    margin-right: auto;
  }

  .action-title{
      margin-left: auto;
      margin-right: auto;
      font-size: 30px;
      line-height: 3rem;
      text-align: center;
  }
  .steps{
    margin-left: auto;
    margin-right: 1rem;
    font-family: 'Mukta', sans-serif;
    color: #839EFF;
    font-weight: bold;
    font-size: 11px;
    text-align: center;
  }

  .steps-text{
    display: block;
    margin-left: auto;
    margin-right: auto;
    text-align: center;
    font-family: 'Montserrat', sans-serif;
    font-size: 15px;
  }

  .carousel{
  background-color: #80C2FF;
  border-radius: 50px;
  width: 97%;
  }


}



@media screen and (max-width: 697px) {

  .title{
    font-family: 'Montserrat', sans-serif;
    margin-left: -2rem;
    font-weight: bold;
    font-size: 16px;
    cursor: pointer;
  }
  .ellipseImg{
    display: block;
    margin-left: 0rem;
    width: 10px;
    
  }

  .nav-links{
    list-style-type: none;
    // margin: 0;
    padding: 0;
    width: 60%;
    
  }

  .nav-links li{
    display: inline;
    padding: 1px 13px;
    font-family: 'Montserrat', sans-serif;
    font-size: 14px;
    color: #001A26;
    cursor: pointer;
    
  }


  .messageImg{
  width: 22px;
  margin-top: -.3rem;

  }

  .userImg{
  width: 32px;
  border-radius: 50%;
  }


  
}


// Media Queries for other devices
// Phone - 600px and below

@media screen and (max-width: 600px) {
  .title{
    font-family: 'Montserrat', sans-serif;
    margin-left: -2rem;
    font-weight: bold;
    font-size: 15px;
    cursor: pointer;
  }
  .ellipseImg{
    display: block;
    margin-left: 0rem;
    width: 10px;
    
  }

  .nav-links{
    list-style-type: none;
    // margin: 0;
    padding: 0;
    width: 65%;
    
  }

  .nav-links li{
    display: inline;
    padding: 1px 8px;
    font-family: 'Montserrat', sans-serif;
    font-size: 13px;
    color: #001A26;
    cursor: pointer;
    
  }

  .action-title{
    font-size: 23px;
  
  }
  .messageImg{
  width: 22px;
  margin-top: -.3rem;

  }

  .userImg{
  width: 32px;
  border-radius: 50%;
  }


  
}

@media screen and (max-width: 503px) {

  .title{
    font-family: 'Montserrat', sans-serif;
    margin-left: -2.2rem;
    font-weight: bold;
    font-size: 13.5px;
    cursor: pointer;
  }
  .ellipseImg{
    display: block;
    margin-left: 0rem;
    width: 9px;
    
  }

  .nav-links{
    list-style-type: none;
    // margin: 0;
    padding: 0;
    width: 60%;
    
  }

  .nav-links li{
    display: inline;
    padding: 1px 6px;
    font-family: 'Montserrat', sans-serif;
    font-size: 11px;
    color: #001A26;
    cursor: pointer;
    
    
  }

  .action-title{
    font-size: 21px;
  
  }
  .messageImg{
  width: 18px;
  margin-top: -.3rem;

  }

  .userImg{
  width: 24px;
  border-radius: 50%;
  }

}

@media screen and (max-width: 399px) {

  .title{
    font-family: 'Montserrat', sans-serif;
    margin-left: -2.6rem;
    font-size: 10px;
    cursor: pointer;
  }
  .ellipseImg{
    display: block;
    margin-left: 0rem;
    width: 7px;
    
  }

  .nav-links{
    list-style-type: none;
    // margin: 0;
    padding: 0;
    width: 60%;
    
  }

  .nav-links li{
    display: inline;
    padding: 1px 4px;
    font-family: 'Montserrat', sans-serif;
    font-size: 10px;
    color: #001A26;
    cursor: pointer;
    
    
  }

  .action-title{
    font-size: 19px;
  
  }
  .messageImg{
  width: 18px;
  margin-top: -.3rem;

  }

  .userImg{
  width: 24px;
  border-radius: 50%;
  }

}



</style>
