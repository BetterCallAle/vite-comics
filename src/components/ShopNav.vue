<script>
export default{
    name: "ShopNav",
    data(){
        return{
            cards: [
                {
                    imgPath: this.getImgPath('../assets/img/buy-comics-digital-comics.png'),
                    imgAlt: "Tablet con all'interno logo DC",
                    cardText: "Digital Comics",
                    href: "/Comics"
                },
                {
                    imgPath: this.getImgPath('../assets/img/buy-comics-merchandise.png'),
                    imgAlt: "T-shirt con logo DC",
                    cardText: "DC Merchandise",
                    href: "/Merchandise"
                },
                {
                    imgPath: this.getImgPath('../assets/img/buy-comics-subscriptions.png'),
                    imgAlt: "Carte con simbolo di Flash",
                    cardText: "Subscription",
                    href: "/Subscription"
                },
                {
                    imgPath: this.getImgPath('../assets/img/buy-comics-shop-locator.png'),
                    imgAlt: "Puntatore mappa",
                    cardText: "Comic Shop Locator",
                    href: "/Locator"
                },
                {
                    imgPath: this.getImgPath('../assets/img/buy-dc-power-visa.svg'),
                    imgAlt: "Carta di credito con simbolo di Flash",
                    cardText: "DC Power Visa",
                    href: "/Visa"
                },
            ]
        }
    },
    methods:{
        getImgPath(path){
            return new URL(path, import.meta.url).href
        }
    }
}
</script>

<template>
    <section id="shop-nav">
        <nav>
            <div class="container">
                <div class="row">
                    <div class="card" v-for="card in cards">
                        <a :href="card.href">
                            <div class="card-img">
                                <img :src="card.imgPath" :alt="card.imgAlt">
                            </div>

                            <div class="card-txt">
                                <h2>{{ card.cardText }}</h2>
                            </div>
                        </a>
                    </div>
                </div>
            </div>
        </nav>
    </section>
</template>

<style lang="scss" scoped>
@use '../styles/partials/mixins' as *;
@use '../styles/partials/variables' as *;

#shop-nav{
    background-color: $main-blue;
    padding: 2rem 0;

    .row{
        @include flex-container(space-evenly);
        .card{
            @include flex-vertical-center();
            width: calc(100% / 5 - 1rem);
            margin-left: 1rem;
            padding: .5rem;
            border: 1px solid transparent;
            border-radius: 10px;
            transition: all 125ms linear;
            
            &:hover{
                    border: 1px solid white;
                    background-color: lighten($main-blue, 10%);
                }

            a{
                display: flex;
                width: 100%;
                height: 100%;
                
                .card-img{
                    width: 25%;
                    @include flex-vertical-center();

                    img{
                        width: 100%;
                        min-width: 40px;
                    }
                }

                .card-txt{
                    margin-left: 1rem;
                    font-size: .6rem;
                    color: white;
                    @include flex-vertical-center();

                    h2{
                        font-weight: 100;
                        text-transform: uppercase;
                    }
                }
            }
        }
    }
}

</style>