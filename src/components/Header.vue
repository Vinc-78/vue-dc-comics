<template>
  <div class="container">
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


<style lang="scss">
@import "../styles/Variables.scss";

.container {
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

    a {
      color: rgb(70, 85, 111);
      text-decoration: none;
    }

    a:hover {
      color: $celestino;

      &::after{ width: 15px;
                background-color: $celestino;}
    }
  }
}
</style>



