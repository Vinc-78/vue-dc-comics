<template>
  <div class="shellFooter">

    <div> <BluLine></BluLine> </div>

    <div class="centralFooter">

        <div class="centralFooter-left">
            <div class="centralFooter-left-list-left">

                <div class="centralFooter-left-list-left-sup">
                    <h2><a href="#">DC COMICS</a></h2>
                    <ul v-for="(element, i) in comicsArray" :key="i">
                        <li><a href="#">{{element}}</a></li>
                    </ul>
                </div>
                <div class="centralFooter-left-list-left-inf">
                    <h2><a href="#">SHOP</a></h2>
                    <ul v-for="(element, i) in shopArray" :key="i">
                        <li><a href="#">{{element}}</a></li>
                    </ul>
                </div>

            </div>
            <div class="centralFooter-left-list-central">
                <h2><a href="#">DC</a></h2>
                <ul v-for="(element, i) in dcArrat" :key="i">
                    <li><a href="#">{{element}}</a></li>
                </ul>

            </div>
            <div class="centralFooter-left-list-right">
                <h2><a href="#">SITES</a></h2>
                <ul v-for="(element, i) in sitesArray" :key="i">
                    <li><a href="#">{{element}}</a></li>
                </ul>

            </div>

        </div>
        <div class="centralFooter-right">
            <img src="../assets/img/dc-logo-bg.png" alt="logo nel footer">
        </div>
      
    </div>
    <div class="navSocial">

        <div class="navSocialContainer">

            <div class="navSocial-left">
            <a href="#">SIGN-UP NOW!</a>

            </div>
            <div class="navSocial-right">
                <span>FOLLOW US</span>
                <ul v-for="(element, i) in socialArray" :key="i">
                    <li><a href="#"><img v-bind:src="require('@/assets/img/'+ element)" alt="face"></a></li>
                    
                </ul>
            
            </div>

        </div>
        
        

    </div>

  </div>
</template>

<script >

import BluLine from "../components/BluLine.vue"


export default {
  name: "Footer",
  
  data(){return{ 
      comicsArray:["Characters","Comics","Movies","TV","Games","Videos","News"],
      shopArray:["Shop DC","Shop DC Collectibles"],
      dcArrat:["Terms Of Use","Privacy policy(New)","Ad Choices","Advertising","Jobs","Subscriptions","Talent Workshops","CPSC Certificates","Ratings","Shop Help","Contact Us"],
      sitesArray:["DC","MAD Magazine","DC Kids","DC Universe","DC Power Visa"],
      socialArray:["footer-facebook.png","footer-twitter.png","footer-youtube.png","footer-pinterest.png","footer-periscope.png"]
      }},

  components: {

  BluLine,
    
    
  }
};
</script>

<style  lang="scss" >
@import "../styles/Variables.scss";

.shellFooter {
  background-image: url("../assets/img/footer-bg.jpg");
  background-repeat: no-repeat;
  background-size: cover;
  height: 100%;
}

.centralFooter {
  padding: $padding;
  width: 960px;
  margin: auto;
  display: flex;
  justify-content: space-between;
  position: relative;
  
  h2{ font-size: 16px;
      margin: 25px 0;

      a{color:white;
        text-decoration: none;}}

  .centralFooter-left-list-central{margin:0px 15px;}

  ul{margin-left:-40px;}

  li{ 
      list-style: none;
            a{ text-decoration: none;
            color:rgb(149, 149, 135);
            font-size: 12px;
            
            }
  }

}

.centralFooter-left {display: flex;}
.centralFooter-right{ z-index: 1;
                     
                     position: absolute;
                     right: -20px;
                     top:-50px;

    
    img{object-fit: cover;
        width: 100%;
        }
}

.navSocial{position:relative;
           
           z-index: 100;
           background-color: rgb(48, 48, 48);}

.navSocialContainer {
           padding: $padding * 2;
           width: 960px;
           margin: auto;
           display: flex;
           justify-content: space-between;
           align-items: center;

    .navSocial-left{ border:1px solid $celestino;
                     padding: $padding ;
                 
                 a{ text-decoration: none;
                    color: white;}
                    
                    }

    .navSocial-right{ padding: $padding ;
                      color: $celestino;
                      font-weight: bold;
                      display: flex;
                      align-items: center;
                     
                      
                      ul{display: inline-block;
                      
                        li{list-style: none;
                           display: inline-block;
                           padding: 0 10px;
                        };}}

}


</style>