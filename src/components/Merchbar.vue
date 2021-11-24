<template>
    <div class="container_full merchbar">
        <div class="container">
            <ul>
                <li v-for="(item, i) in shopItems" :key="`shop_item${i}`">
                    <img :src="item.img" alt="buy digital comics" class="shop_item_img" >
                    <a :href="`${item.url}`"> {{item.text}} </a>
                </li>
            </ul>
        </div>
    </div>
</template>

<script>
export default {
    name: 'Merchbar',
    data() {
        return {
            shopItems: [
                {
                    img: require('@/assets/img/merch-bar/buy-comics-digital-comics.png'),
                    text: 'digital comics',
                    url: '/shop',
                },
                {
                    img: require('@/assets/img/merch-bar/buy-comics-merchandise.png'),
                    text: 'dc merchandise',
                    url: '/merchandise',
                },
                {
                    img: require('@/assets/img/merch-bar/buy-comics-shop-locator.png'),
                    text: 'subscription',
                    url: '/subscriptions',
                },
                {
                    img: require('@/assets/img/merch-bar/buy-comics-subscriptions.png'),
                    text: 'comic shop locator',
                    url: '/locator',
                },
                {
                    img: require('@/assets/img/merch-bar/buy-dc-power-visa.svg'),
                    text: 'dc power visa',
                    url: '/power_visa',
                },
            ],
        };
    },
}
</script>

<style scoped lang="scss">
@import '@/styles/vars.scss';
    .container_full {
        background-color: $brand_color;
        .container {
            height: 100%;
            padding: 35px 20px;
            display: flex;
            align-items: center;
            // justify-content: space-between;
            
            ul {
                width: 100%;
                display: flex;
                justify-content: space-between;
                // align-items: center;
                color: white;
                li {
                    display: flex;
                    align-items: center;
                    width: calc(100% / 5);
                    img {
                    max-width: 35px;
                    }
                    a {
                        text-decoration: none;
                        text-transform: uppercase;
                        color: currentColor;
                        font-size: .60rem;
                        font-weight: 400;
                        font-family: sans-serif;
                        margin-left: 20px;
                    }
                }
                
            }
        }
    }
</style>