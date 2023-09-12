<script>
    export default {
        data() {
            return {
                products : [
                    {
                    linkName: "DIGITAL COMICS",
                    url: "#",
                    img: "src/assets/img/buy-comics-digital-comics.png",
                    },
                    {
                    linkName: "DC MERCHNDISE",
                    url: "#",
                    img: "src/assets/img/buy-comics-merchandise.png",
                    },
                    {
                    linkName: "SUBSCRIPTION",
                    url: "#",
                    img: "src/assets/img/buy-comics-subscriptions.png",
                    },
                    {
                    linkName: "COMIC SHOP LOCATOR",
                    url: "#",
                    img: "src/assets/img/buy-comics-shop-locator.png",
                    },
                    {
                    linkName: "DC POWER VISA",
                    url: "#",
                    img: "src/assets/img/buy-dc-power-visa.svg",
                    },
                ],
            }
        }
    }
</script>

<template>
    <div class="product container">
        <div class="product-list">
            <div class="product-item" v-for="product in products" >
                <div class="links" :href="product.url">
                    <div class="product-image">
                        <a :href="product.url">
                            <img :src= "product.img">
                        </a>
                    </div>
                    <a :href="product.url">
                        <p>{{ product.linkName }}</p>
                    </a>
                </div>
            </div> 
        </div>
        </div>
</template>

<style lang="scss" scoped>
// GENERAL STYLE
  @use '../assets/styles/general.scss' as *;

//   VARIABLES
  @use '../assets/styles/partials/variables' as *;

.product {
    background-color: $primary-color;

    .product-list {
        display: flex;
        justify-content: space-evenly;
        
        .product-item{
            padding-top: 2rem;
            padding-bottom: 2rem;
            margin-right: 2rem;

          
        .links {
            display: flex;
            align-items: center;

            font-weight: 700;

            p {
                color: $white-text;
            }
            .product-image {
                width: 50px;
                height: 55px;

                margin-right: 1rem;

                img {
                    height: 100%;
                }
            }
        }
        }
    }
}


</style>