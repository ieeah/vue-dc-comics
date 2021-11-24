<template>
  <div class="container_full">
      <div class="container footer">
          <div class="col">
            <h3>DC COMICS</h3>
            <ul>
                <li class="foot_link" v-for="(link, index) in footerLinkLeft" :key="`col1_link-${index}`">
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
                <li class="foot_link" v-for="(link, index) in footerLinkRight" :key="`col2_link-${index}`">
                    <a :href="`${link.url}`">{{link.text}}</a>
                </li>
            </ul>
          </div>
          <div class="col">
            <h3>SITES</h3>
            <ul>
                <li class="foot_link" v-for="(link, index) in footerSites" :key="`col3_link-${index}`">
                    <a :href="`${link.url}`">{{link.text}}</a>
                </li>
            </ul>
          </div>
          <div class="col_right">

          </div>
      </div>
      <div class="sub_footer">
          <div class="container">
              <a class="sign_button">SIGN-UP NOW!</a>
              <div class="footer_socials">
                  <ul>
                    <li><a href="" id="follow_us">FOLLOW US</a></li>
                    <li>
                        <a href="">
                            <img src="@/assets/img/footer/footer-facebook.png" alt="">
                        </a>
                    </li>
                    <li>
                        <a href="">
                            <img src="@/assets/img/footer/footer-twitter.png" alt="">
                        </a>
                    </li>
                    <li>
                        <a href="">
                            <img src="@/assets/img/footer/footer-youtube.png" alt="">
                        </a>
                    </li>
                    <li>
                        <a href="">
                            <img src="@/assets/img/footer/footer-pinterest.png" alt="">
                        </a>
                    </li>
                    <li>
                        <a href="">
                            <img src="@/assets/img/footer/footer-periscope.png" alt="">
                        </a>
                    </li>
                  </ul>
              </div>
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
@import '@/styles/vars.scss';
.container_full {
    width: 100%;
    background-image: url(../assets/img/footer/footer-bg.jpg);
    background-size: cover;
    background-position: center;
    color: white;

}

.container.footer {
    display: flex;
    margin-inline: auto;
    justify-content: center;
    overflow: hidden;
    h3 {
        font-weight: 400;
    }

    ul {
        margin-block: 10px;
        li {
        display: block;
            a {
                color: lightgrey;
                text-decoration: none;
                font-weight: 200;
                text-transform: capitalize;
                font-size: .85rem;

                &:hover {
                    color: white;
                }
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
            bottom: 0%;
            right: -25%;
            background-image:url(../assets/img/footer/dc-logo-bg.png);
            background-repeat: no-repeat;
            transform: scale(1.15);
        }
    }
}

.sub_footer {
    background-color: #303030;
    display: flex;
    justify-content: space-between;
    align-items: center;
    width: 100%;
    
    .container {
        display: flex;
        align-items: center;
        justify-content: space-between;
        padding-block: 35px;
        a.sign_button {
            display: flex;
            align-items: center;
            text-align: center;
            height: fit-content;
            background-color: transparent;
            border: 2px solid $brand_color;
            padding: 7px 17px;
            cursor: pointer;
            transition: all .1s ease;
            &:hover {
                background-color: rgba($color: white, $alpha: .2);
                border-color: white;
            }
        }
    }
    .footer_socials {
        display: flex;
        ul {
            display: flex;
            align-items: center;
                li {
                display: inline-block;
                margin-left:15px;
                #follow_us {
                    font-size: 1.2rem;
                    padding-right: 10px;
                    font-weight: 400;
                    color: $brand-color;
                }
                a {
                    color: lightgrey;
                    text-decoration: none;
                    font-weight: 200;
                    text-transform: capitalize;
                    &:hover {
                    filter: brightness(150%);
                }
                }
            }
        }
        
    }
}
</style>