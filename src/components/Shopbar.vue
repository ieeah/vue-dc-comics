<template>
  <div class="container_full">
      <div class="container">
          <ul>
                <li v-for="(item, i) in shopItems" :key="`shop_item${i}`">
                    <img class="shop_item_img" :src="require(`../assets/dc-comics-assets/img/merch-bar/${item[i].img}`)" alt="buy digital comics">
                    <a :href="`${item[i].url}`"></a>
              </li>
          </ul>
      </div>
  </div>
</template>

<script>
export default {
    name: 'Shopbar',
    data() {
        return {
            shopItems: [
                {
                    img: 'buy-comics-digital-comics.png',
                    text: 'digital comics',
                    url: '/shop',
                },
                {
                    img: 'buy-comics-merchandise.png',
                    text: 'dc merchandise',
                    url: '/merchandise',
                },
                {
                    img: 'buy-comics-shop-locator.png',
                    text: 'subscription',
                    url: '/comics',
                },
                {
                    img: 'buy-comics-subscriptions.png',
                    text: 'comic shop locator',
                    url: '/subscriptions',
                },
                {
                    img: 'buy-dc-power-visa.png',
                    text: 'dc power visa',
                    url: '/power_visa',
                },
            ],
        };
    },
}
</script>

<style scoped lang="scss">
    .container_full {
        background-color: #0282f9;

        .container {
            height: 100%;
            background-color: rgba($color: #000000, $alpha: .5);
            padding: 50px;

            ul {
                display: flex;
                justify-content: space-between;
            }
        }
    }
</style>