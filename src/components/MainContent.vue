<script>
import ComicsCardVue from './ComicsCard.vue';

export default{
    name: "MainContent",
    components:{
        ComicsCardVue
    },
    data(){
        return{

        }
    }
}
</script>

<template>
    <section id="main-content">
        <div class="jumbotron"></div>

        <div class="comics">
            <div class="container">
                <div class="row">
                    <ComicsCardVue />
                </div>
            </div>
        </div>
    </section>
</template>

<style lang="scss" scoped>
@use '../styles/partials/mixins' as *;
@use '../styles/partials/variables' as *;

#main-content{
    background-color: $main-dark;
    margin-top: $header-height;
    color: white;

    .jumbotron{
        background-image: url(../assets/img/jumbotron.jpg);
        min-height: 450px;
        background-position: top center;
    }
}


</style>