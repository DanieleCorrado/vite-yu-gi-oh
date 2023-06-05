<script>

export default {
  components: {
    name: "AppHeader"
  }
}

</script>

<template>
  
  <header>
    <div id="logo">
      <img src="../assets/img/Yu-Gi-Oh!_(Logo).png" alt="">

      <h1>  Yu-Gi-Oh API </h1>
    </div>
  </header>

</template>

<style lang="scss" scoped>

header {
  background-color: white;
  padding: 10px;

  #logo {
    display: flex;
    align-items: center;

    img {
      width: 10%;
      margin-right: 20px;
    }

  }
}

</style>
