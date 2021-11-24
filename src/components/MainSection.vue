<template>
  <section class="container_full">
    <div class="jumbo">
      <img src="@/assets/img/jumbotron.jpg" alt="">
    </div>
    <section class="container current_series">
      <div class="floating_title">
        <h2>CURRENT SERIES</h2>
      </div>
      <ul>
        <li v-for="(magazine, i) in CurrentSeries" :key="`magazine_${i}`">
          <Comiccard :url="magazine.thumb" :title="magazine.series"/>
        </li>
      </ul>
    </section>
  </section>
</template>

<script>
import Comicslist from '@/assets/Js/dc-comics.js';
import Comiccard from '@/components/Comic.vue';
export default {
  name: 'MainSection',
  components: {
    Comiccard,
  },

  data() {
    return {
      CurrentSeries: Comicslist,
    };
  },
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
            img {
              height: 100%;
              width: 100%;
              object-fit: cover;
              object-position: top left;
            }
          }

        .container.current_series {
          display: flex;
          margin-inline: auto;
          width: 70%;
          height: 150px;
          background-color: yellow;
            .floating_title {
              background-color: $brand-color;
              padding: 8px 20px;
              height: 60px;
              width: 230px;
              display: flex;
              justify-content: center;
              align-items: center;
              font-size: 1.3rem;
              transform: translateX(-20px) translateY(-85%);
            }
        }
    }
</style>