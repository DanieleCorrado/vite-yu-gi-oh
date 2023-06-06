<script>

export default {
    name: "SingleCard",
    props: {
      details: Object
    }
}
</script>

<template>

  <div class="card">
    <img :src="details.card_images[0].image_url" alt="Immagine carta">
    <h3 class="card-name">{{details.name}}</h3>
    <h5 class="card-type">{{details.type}}</h5>
  </div>


</template>

<style lang="scss" scoped>

.card {
      color: black;
      width: calc((100% / 5) - 10px);
      background-color: rgb(212, 143, 56);
      margin-right: 10px;
      margin-bottom: 10px;

      .card-name {
        margin: 10px 0;
        text-align: center;
        font-size: 25px;
        padding: 0 10px;
        color: white;
      }
      .card-type{
        font-size: 20px;
        text-align: center;
        margin-bottom: 20px;
      }
    }

</style>
