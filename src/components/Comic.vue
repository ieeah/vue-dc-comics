<template>
  <div class="comic_card">
      <div class="comic_cover">
          <img :src="url" :alt="title">
      </div>
      <h4 class="comic_title"> {{title}} </h4>
  </div>
</template>

<script>

export default {
    name: 'Comiccard',
    props: {
        url: String,
        title: String,
    },
}
</script>

<style scoped lang="scss">
.comic_card {
    margin-bottom: 10px;
    .comic_cover {
        width: 100%;
        aspect-ratio: 1 / 1;
        img {
            width: 100%;
            height: 100%;
            object-fit: cover;
            object-position: top left;
            margin-block: 15px;
        }
    }
}
</style>