<template>
    <section class="container">
        <a class="brand" href="/">
            <img src="@/assets/dc-comics-assets/img/header/dc-logo.png" alt="">
        </a>
        <nav>
            <ul>
                <li class="nav_link" v-for="(link, index) in navLinks" :key="`nav_link-${index}`">
                    <a :href="`${link.url}`">{{link.text}}</a>
                </li>
            </ul>
        </nav>
    </section>
</template>

<script>
export default {
    name: 'Header',
    data() {
        return {
            navLinks: [
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
            currentPage: 0,
        };
    },
}
</script>

<style scoped lang="scss">
    .container {
        display: flex;
        justify-content: space-between;
        height: 100px;
        a.brand {
            img {
                padding-block: 15px;
                height: 100%;
            }
        }

        nav {
            height: 100%;
            width: 60%;

            ul {
                display: flex;
                justify-content: space-between;
                align-items: center;
                height: 100%;
            }
            li {
                display: flex;
                align-items: center;
                text-transform: uppercase;
                height: 100%;
                margin-inline: 10px;
                border-bottom: 3px solid transparent;
                &:hover,
                &:active {
                    border-bottom-color: #0282f9;
                    cursor: pointer;
                }
                a {
                    text-decoration: none;
                    color: currentColor;
                }
            }
        }
    }
</style>