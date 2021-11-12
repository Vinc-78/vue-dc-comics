<template>
  <div class="fumetto-singolo">

    <img :src="url" alt="">
    <h4>{{ titolo }}</h4>

    

    <div class="overlay">
      <p><strong>Tipo: </strong>{{ genere }}</p>
      <p><strong>Prezzo: </strong>{{ prezzo }}</p>
    </div>
  </div>
</template>

<script>
export default {
  name: "SingleComic",
  
  props: ["url","prezzo","titolo","genere"],
 
  
  
};
</script>


<style  lang="scss" >
@import "../styles/Variables.scss";


 .fumetto-singolo {
      
      flex-basis: calc( 100% / 6 - 15px );
      position: relative;

      &:hover {
        .overlay {
          opacity: 1;
        }
      }

      img {
        width: 100%;
        height: 50%;
        object-fit: cover;
        object-position: top;
      }

      .overlay {
        position: absolute;
        left: 0;
        top: 0;
        width: 100%;
        height: 70%;
        opacity: 0;
        background-color: rgba(0, 0, 0, 0.3);
        backdrop-filter: blur(5px);
        transition: opacity 0.3s;
        color:white;
        text-align: center;
        text-shadow: 2px 2px black;

      }
    }
  

</style>

