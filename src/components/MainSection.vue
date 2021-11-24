<template>
  <section class="container_full">
    <div class="jumbo">
      <img src="@/assets/img/jumbotron.jpg" alt="">
    </div>
    <section class="current_series"></section>
  </section>
</template>

<script>
export default {
  name: 'MainSection',
}
</script>

<style scoped lang="scss">
@import '@/styles/vars.scss';
    .container_full {
          width: 100vw;
          background-color: black;
          color: white;
          .jumbo {
            height: 400px;
            background-color: yellow;
            img {
              height: 100%;
              width: 100%;
              object-fit: cover;
              object-position: top left;
            }
          }

        .container {
          margin-inline: auto;
          width: 70%;
        }
    }
</style>