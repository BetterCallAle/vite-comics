<script>
export default{
    name: "ComicsCard",
    prompt: {
        imgUrl : String,
        cardHeading : String
    }
}

</script>

<template>
    <div class="card">
        <a href="">
            <div class="card-img">
                <img :src="imgUrl" :alt="'Copertina di ${cardHeading}'">
            </div>

            <div class="card-txt">
                <h3>{{ cardHeading }}</h3>
            </div>
        </a>
    </div>
</template>

<style lang="scss" scoperd>
.card{
    width: calc(100% / 6 - 1rem);
    margin: 1rem .5rem;

    .card-img{
        height: 200px;
        overflow-y: hidden;
        margin-bottom: .8rem;
    }
}

</style>