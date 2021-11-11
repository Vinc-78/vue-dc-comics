<template>
  <div class="containerHeader">
    <div class="logo"><img src="../assets/img/dc-logo.png" alt="" /></div>
    <div class="nav">
      <ul>
        <li v-for="(elemento, i) in link" :key="i">
          <a href="elemento.href">{{ elemento.descrizione }}</a>
        </li>
      </ul>
    </div>
  </div>
</template>

<script >
export default {
  name: "Header",

  data() {
    return {
      link: [
        { href: "#", descrizione: "CHARACTERS" },
        { href: "#", descrizione: "COMICS" },
        { href: "#", descrizione: "MOVIES" },
        { href: "#", descrizione: "TV" },
        { href: "#", descrizione: "GAMES" },
        { href: "#", descrizione: "COLLECTIBLES" },
        { href: "#", descrizione: "VIDEOS" },
        { href: "#", descrizione: "FANS" },
      ],
    };
  },
};
</script>


<style  lang="scss">
@import "../styles/Variables.scss";

.containerHeader {
  width: 960px;
  margin: auto;
  padding: $padding;
  display: flex;
  justify-content: space-between;
  align-items: center;

  img {
    width: 60%;
  }

  li {
    display: inline-block;
    margin: 15px;
    position: relative;

    a {
      color: rgb(70, 85, 111);
      text-decoration: none;
      font-weight: bold;
    }

    a:hover {
      color: $celestino;
    }
    &:hover::after {
      content: "";
      position: absolute;
      bottom: -40px;
      left: 0;
      width: 35px;
      height: 5px;
      background-color: #0282f9;
    }
  }
}
</style>



