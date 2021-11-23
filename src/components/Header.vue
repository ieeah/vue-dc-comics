<template>
  <section>
      <img src="@/assets/dc-comics-assets/img/header/dc-logo.png" alt="">
      <nav>

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
                    text: '',
                    url: '',
                    current: true,
                },
            ],
            merchBar: [],
            footerLink: [],
        };
    },
}
</script>

<style scoped lang="scss">
    section {
        display: flex;
        justify-content: space-between;
        padding-block: 15px;
        height: 100px;

        nav {
            height: 100%;
            width: 50%;
            background-color: red;
        }
    }
</style>