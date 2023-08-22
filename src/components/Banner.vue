<script>
export default {
    data() {
        return {
            bannerLinks: [
                {
                    image:"../src/assets/img/buy-comics-digital-comics.png",
                    name: "Digital Comics",
                },
                {
                    image: "../src/assets/img/buy-comics-merchandise.png",
                    name: "DC Merchandise",
                },
                {
                    image: "../src/assets/img/buy-comics-subscriptions.png",
                    name: "Subscription",
                },
                {
                    image: "../src/assets/img/buy-comics-shop-locator.png",
                    name: "Comic Shop Locator",
                },
                {
                    image: "../src/assets/img/buy-dc-power-visa.svg",
                    name: "DC Power Visa",
                }
            ]
        }
    },
}
</script>

<template>
    <div class="banner-wrapper">
        <div class="container d-flex my-banner-container">
            <div class="banner-item" v-for="banner in bannerLinks">
                <img v-bind:src="banner.image" alt="">
                <div class="banner-title">{{ banner.name.toUpperCase() }}</div>
            </div>
        </div>
    </div>
</template>

<style lang="scss" scoped>
.banner-wrapper {
    background-color: #0282F9;
    padding: 3.4rem;

    .my-banner-container{
        padding: 0px 40px;
    }

    .banner-item{
        justify-content: center;
        align-items: center;
        display: flex;
        padding-right: 1.3rem;
    }
    img{
        width: 70px;
        padding-right: 1rem;
    }
    .banner-title{
        color: white;
    }
}
</style>