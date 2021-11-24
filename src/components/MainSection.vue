<template>
  <section class="container_full">
    <div class="jumbo">
      <img src="@/assets/img/jumbotron.jpg" alt="">
    </div>
    <section class="container current_series">
      <div class="floating_title">
        <h2>CURRENT SERIES</h2>
      </div>
      <ul class="magazines_list">
        <li v-for="(magazine, i) in CurrentSeries" :key="`magazine_${i}`">
          <Comiccard :url="magazine.thumb" :title="magazine.series"/>
        </li>
      </ul>
            <a href="" class="load_more_btn">LOAD MORE</a>
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
          background-color: #1c1c1c;
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
          flex-direction: column;
          margin-inline: auto;
          align-items: center;
          width: 70%;
          position: relative;
          padding-top: 50px;
            .floating_title {
              background-color: $brand-color;
              padding: 8px 20px;
              height: 60px;
              display: flex;
              justify-content: center;
              align-items: center;
              font-size: 1.3rem;
              position: absolute;
              left: -20px;
              top: -30px;
              
            }
            ul.magazines_list {
                width: 100%;
              display: flex;
              flex-wrap: wrap;
              li {
                display: inline-block;
                width: calc(100% / 6);
                padding: 8px;
              }
            }
            .load_more_btn {
                text-decoration: none;
                color: currentColor;
                background-color: $brand-color;
                padding: 10px 45px;
                margin-bottom: 20px;
            }
        }
    }
</style>