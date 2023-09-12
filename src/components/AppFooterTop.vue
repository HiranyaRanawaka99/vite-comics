<script>
    export default {
        data() {
            return {
                links: [
                    {
                    title: "DC COMICS",
                    footerLinks: [
                        "Characters",
                        "Comics",
                        "Movies",
                        "TV",
                        "Games",
                        "Videos",
                        "News",
                        ],
                    },
                    {
                    title: "DC",
                    footerLinks: [
                        "Terms Of Use",
                        "Privacy policy (New)",
                        "Ad Choices",
                        "Advertising",
                        "Jobs",
                        "Subscriptions",
                        "Talent Workshops",
                        "CPSC Certificates",
                        "Ratings",
                        "Shop Help",
                        "Contact Us",
                        ],
                    },
                    {
                    title: "SITES",
                    footerLinks: [
                        "DC",
                        "MAD Magazine",
                        "DC Kids",
                        "DC Universe",
                        "DC Power Visa",
                        ],
                    },
                    {
                    title: "SHOP",
                    footerLinks: ["Shop DC", 
                                "Shop DC Collectibles"
                            ],
                    },
                 ],
                 backgroundLogo: {
                    src: 'src/assets/img/dc-logo-bg.png'
                 }
            }
        }
    }
</script>

<template>
    <div class= "footer container">
        <div class = "links">
            <div v-for ="link in links">
                <h4> {{ link.title }} </h4>
                <ul v-for="footerLink in link.footerLinks">
                    <li> <a href="#">{{ footerLink }} </a></li>
                </ul>
            </div>
        </div>
        <div class="footer-logo"> 
            <img :src = "backgroundLogo.src">
        </div>
    </div>
</template>

<style lang="scss" scoped>
// GENERAL STYLE
  @use '../assets/styles/general.scss' as *;

//   VARIABLES
  @use '../assets/styles/partials/variables' as *;

    .footer.container {
        background-image: url(../assets/img/footer-bg.jpg);
        background-size: cover;

        display: flex;

        .links {
            width: 50%;
            padding-top: 2rem;
            padding-bottom: 2rem;

            display: flex;
            flex-wrap: wrap;
            gap: 2rem;

            color: $grey-text;

            
            h4 {
                padding-bottom: .5rem;
                color: $white-text;
            }

            a {
                color: $grey-text;
            }
        }
        .footer-logo {
            display: flex;
            justify-content: end;

            width: 700px;
            height: 350px;

            img {
                object-fit: none;
            }

        }
    }
    

</style>