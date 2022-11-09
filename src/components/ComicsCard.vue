<script>
export default{
    name: "ComicsCard",
    props: {
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
    width: calc(100% / 6 - 1.5rem);
    margin: 1rem .75rem;

    &:hover .card-img img{
        scale: 1.1
    }

    .card-img{
        height: 200px;
        overflow: hidden;
        margin-bottom: .8rem;

        img{
            scale: 1;
            transition: all 300ms linear;
        }
    }

    .card-txt{
        font-size: .7rem;
        text-transform: uppercase;
        h3{
            font-weight: 100;
        }
    }
}

</style>