<template>
  <div class="shell">
    <div class="container">
      <div class="h1">-->Content Goes Here >--</div>
    </div>
  </div>
</template>

<script >
export default {
  name: "Main",
};
</script>

<style scoped lang="scss" >
@import "../styles/Variables.scss";


.container {
  padding: $padding;

  color: white;
}

.shell {
    background-color: $dark;
    padding: $padding;
}
</style>

