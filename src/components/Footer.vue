<template>
  <div class="container_full">
      <div class="container">
          <div class="col">
            <h3>DC COMICS</h3>
            <ul>
                <li class="foot_link" v-for="(link, index) in footerLinkLeft" :key="`nav_link-${index}`">
                    <a :href="`${link.url}`">{{link.text}}</a>
                </li>
            </ul>
            <h3>SHOP</h3>
            <ul>
                <li>
                    <a href="/shop">Shop DC</a>
                </li>
                <li>
                    <a href="/shop_collectibles">Shop DC Collectibles</a>
                </li>
            </ul>
          </div>
          <div class="col">
            <h3>DC</h3>
            <ul>
                <li class="foot_link" v-for="(link, index) in footerLinkRight" :key="`nav_link-${index}`">
                    <a :href="`${link.url}`">{{link.text}}</a>
                </li>
            </ul>
          </div>
          <div class="col">
            <h3>SITES</h3>
            <ul>
                <li class="foot_link" v-for="(link, index) in footerSites" :key="`nav_link-${index}`">
                    <a :href="`${link.url}`">{{link.text}}</a>
                </li>
            </ul>
          </div>
          <div class="col_right">

          </div>
      </div>
      <div class="sub_footer">
          <div class="container">
              
          </div>
      </div>
  </div>
</template>

<script>
export default {
    name: 'Footer',
    data() {
        return {
            footerLinkLeft: [
                {
                    text: 'Characters',
                    url: '/characters',
                    current: true,
                },
                {
                    text: 'Comics',
                    url: '/comics',
                    current: false,
                },
                {
                    text: 'movies',
                    url: '/movies',
                    current: false,
                },
                {
                    text: 'tv',
                    url: '/tv',
                    current: false,
                },
                {
                    text: 'games',
                    url: '/games',
                    current: false,
                },
                {
                    text: 'collectibles',
                    url: '/collectibles',
                    current: false,
                },
                {
                    text: 'videos',
                    url: '/videos',
                    current: false,
                },
                {
                    text: 'fans',
                    url: '/fans',
                    current: false,
                },
                {
                    text: 'news',
                    url: '/news',
                    current: false,
                },
                {
                    text: 'shop',
                    url: '/shop',
                    current: false,
                },
            ],
            footerLinkRight: [
                {
                    text: 'terms of use',
                    url: '/terms',
                    current: true,
                },
                {
                    text: 'Privacy policy (new)',
                    url: '/privacy',
                    current: false,
                },
                {
                    text: 'Ad choices',
                    url: '/ad_choices',
                    current: false,
                },
                {
                    text: 'advertising',
                    url: '/advertising',
                    current: false,
                },
                {
                    text: 'games',
                    url: '/games',
                    current: false,
                },
                {
                    text: 'jobs',
                    url: '/jobs',
                    current: false,
                },
                {
                    text: 'subscriptions',
                    url: '/subscriptions',
                    current: false,
                },
                {
                    text: 'talent workshops',
                    url: '/workshops',
                    current: false,
                },
                {
                    text: 'CPSC Certificates',
                    url: '/ratings',
                    current: false,
                },
                {
                    text: 'shop help',
                    url: '/shop_help',
                    current: false,
                },
                {
                    text: 'contact us',
                    url: '/contacts',
                    current: false,
                },
            ],
            footerSites: [
                {
                    text: 'DC',
                    url: '/',
                    current: true,
                },
                {
                    text: 'MAD Magazine',
                    url: '/mad',
                    current: false,
                },
                {
                    text: 'DC kids',
                    url: '/dc_kids',
                    current: false,
                },
                {
                    text: 'dc_universe',
                    url: '/dc_universe',
                    current: false,
                },
                {
                    text: 'DC Power visa',
                    url: '/power_visa',
                    current: false,
                },
            ],
            currentPage: 0,
        };
    },
}
</script>

<style scoped lang="scss">
    .container_full {
        width: 100%;
        background-image: url(../assets/dc-comics-assets/img/footer/footer-bg.jpg);
        background-size: cover;
        background-position: center;
        color: white;

    }

    .container {
        display: flex;
        margin-inline: auto;
        justify-content: center;
        overflow: hidden;
        h3 {
            font-weight: 300;
        }

        ul {
            margin-block: 10px;
            li {
            display: block;
                a {
                    color: grey;
                    text-decoration: none;
                    font-weight: 200;
                    text-transform: capitalize;
                }
            }
        }
        
        .col {
            padding: 35px;
            padding-left: 0;
            width: calc(40% / 3);
        }
        
        .col_right {
            margin-inline: auto;
            width: 60%;
            position: relative;
            &::after {
                content: '';
                width: 100%;
                height: 120%;
                position: absolute;
                right: -25%;
                top: -10%;
                background-image:url(../assets/dc-comics-assets/img/footer/dc-logo-bg.png);
                background-repeat: no-repeat;
                transform: scale(1.1);
            }
        }
    }

</style>