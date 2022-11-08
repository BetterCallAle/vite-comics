<script>
name: "AppHeader"
export default{
    data(){
        return{
            links:[
                {
                    text: "Characters",
                    href: "/Characters",
                    active: false
                },
                {
                    text: "Comics",
                    href: "/Comics",
                    active: true
                },
                {
                    text: "Movies",
                    href: "/Movies",
                    active: false
                },
                {
                    text: "TV",
                    href: "/TV",
                    active: false
                },
                {
                    text: "Games",
                    href: "/Games",
                    active: false
                },
                {
                    text: "Collectibles",
                    href: "/Collectibles",
                    active: false
                },
                {
                    text: "Videos",
                    href: "/Videos",
                    active: false
                },
                {
                    text: "Fans",
                    href: "/Fans",
                    active: false
                },
                {
                    text: "News",
                    href: "/News",
                    active: false
                },
                {
                    text: "Shop",
                    href: "/Shop",
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
    height: 150px;
    line-height: 150px;
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
                        line-height: 136px;
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