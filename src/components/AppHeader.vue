<script>
name: "AppHeader"
export default{
    data(){
        return{
            links:[
                {
                    text: "Characters",
                    href: "/characters",
                    active: false
                },
                {
                    text: "Comics",
                    href: "/comics",
                    active: true
                },
                {
                    text: "Movies",
                    href: "/movies",
                    active: false
                },
                {
                    text: "TV",
                    href: "/tv",
                    active: false
                },
                {
                    text: "Games",
                    href: "/games",
                    active: false
                },
                {
                    text: "Collectibles",
                    href: "/collectibles",
                    active: false
                },
                {
                    text: "Videos",
                    href: "/videos",
                    active: false
                },
                {
                    text: "Fans",
                    href: "/fans",
                    active: false
                },
                {
                    text: "News",
                    href: "/news",
                    active: false
                },
                {
                    text: "Shop",
                    href: "/shop",
                    active: false
                }
            ],
            currentActiveItem: 1
        }
    },
    methods:{
            // Change the active element in the list
            changeActiveElement(index){
                // set the current active element false
                this.links[this.currentActiveItem].active = false;
                // make the current active elemetn = index
                this.currentActiveItem = index;
                // set the clicked element true
                this.links[index].active = true
            }
        }
}
</script>


<template>
    <header>
        <div class="container">
            <div class="header-logo">
                <img src="../assets/img/dc-logo.png" alt="Logo DC">
            </div>

            <nav class="header-nav">
                <ul>
                    <li v-for="(link, index) in links" :key="index" @click="changeActiveElement(index)">
                        <a :class="{'active': link.active}" :href="link.href">{{ link.text }} </a>
                    </li>
                </ul>
            </nav>
        </div>
    </header>
</template>

<style lang="scss" scoped>
@use '../styles/partials/variables' as *;
@use '../styles/partials/mixins' as *;

header{
    height: 120px;
    line-height: 120px;
    .container{
        @include flex-container(space-between);
        
        .header-logo{
            img{
                vertical-align: middle
            }
        }

        nav{
            ul{
                @include flex-container(space-between);
                gap: 1rem;

                li{
                    a{
                        display: inline-block;
                        text-transform: uppercase;
                        line-height: 105px;
                        color: lighten($main-dark, 20%);
                        font-weight: 700;
                        font-size: .8rem;
                        cursor: pointer;
                        &.active{
                            border-bottom: 7px solid $main-blue;
                            color: $main-blue;
                        }
                    }
                }
            }
        }
    }
    
}
</style>