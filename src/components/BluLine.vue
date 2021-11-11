<template>
  <div class="shellBlu">
    <div class="containerBlu">
      <div class="navBlu">
        <ul>
          <li>
            <div class="img">
              <img
                src="../assets/img/buy-comics-digital-comics.png"
                alt="img"
              />
            </div>
            <a href="#">DIGITAL COMICS</a>
          </li>
          <li>
            <div class="img">
              <img src="../assets/img/buy-comics-merchandise.png" alt="img" />
            </div>
            <a href="#">DC MERCHANDISE</a>
          </li>
          <li>
            <div class="img">
              <img src="../assets/img/buy-comics-subscriptions.png" alt="img" />
            </div>
            <a href="#">SUBSCRIPTION</a>
          </li>
          <li>
            <div class="img">
              <img src="../assets/img/buy-comics-shop-locator.png" alt="img" />
            </div>
            <a href="#">COMIC SHOP LOCATOR</a>
          </li>
          <li>
            <div class="img">
              <img src="../assets/img/buy-dc-power-visa.svg" alt="img" />
            </div>
            <a href="#">DC POWER VISA</a>
          </li>
        </ul>
      </div>
    </div>
  </div>
</template>

<script >
export default {
  name: "BluLine",
};
</script>

<style  lang="scss" >
@import "../styles/Variables.scss";

.containerBlu {
  width: 980px;
  margin: auto;
  padding: 20px 0;
  display: flex;
  justify-content: space-between;
  align-items: center;
  z-index: 100;

  .img {
    width: 65px;
    margin-left: 5px;
    display: inline-block;
    vertical-align: middle;

    img {
      object-fit: cover;
      width: 60%;
    }
  }

  ul {
    list-style: none;

    li {
      display: inline-block;
    }
    a {
      font-size: 12px;
      color: white;
      text-decoration: none;
      padding-right: 5px;
    }
  }
}
.navBlu {
  text-align: center;
}

.shellBlu {
  background-color: $celestino;
}
</style>

