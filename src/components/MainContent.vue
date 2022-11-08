<script>
export default{
    name: "MainContent",
    data(){
        return{

        }
    }
}
</script>

<template>
    <section id="main-content">
        <div class="container">
            <h2> --> Content Goes Here &lt;-- </h2>
        </div>
    </section>
</template>

<style lang="scss" scoped>
@use '../styles/partials/mixins' as *;
@use '../styles/partials/variables' as *;

#main-content{
    background-color: $main-dark;
    padding: 4rem 0;
    color: white;
}


</style>