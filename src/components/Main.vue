<template>
  <div class="shell">
    <div class="containerMain">
      <div class="h1">-- Content Goes Here --</div>
    </div>
  </div>
</template>

<script >
export default {
  name: "Main",
};
</script>

<style  lang="scss" >
@import "../styles/Variables.scss";

.containerMain {
  padding: $padding;
  width: 960px;
  margin: auto;

  color: white;
}

.shell {
  background-color: $dark;
  padding: $padding;
}
</style>

