<script>
export default{
    name: "AppFooter",
    data(){
        return{
        }
    }
}
</script>

<template>
    <footer>
        <!-- FOOTER TOP -->
        <div class="footer-top">
            <div class="container">
                <!-- FOOTER TOP LEFT -->
                <div class="footer-top-left">
                    <nav class="nav-left">
                        <h3>DC COMICS</h3>
                        <ul>
                            <li>
                                <a href="#">Characters</a>
                            </li>

                            <li>
                                <a href="#">Comics</a>
                            </li>

                            <li>
                                <a href="#">Movies</a>
                            </li>

                            <li>
                                <a href="#">TV</a>
                            </li>

                            <li>
                                <a href="#">Games</a>
                            </li>

                            <li>
                                <a href="#">Videos</a>
                            </li>

                            <li>
                                <a href="#">News</a>
                            </li>
                        </ul>

                        <h3>SHOP</h3>
                        <ul>
                            <li>
                                <a href="#">Shop DC</a>
                            </li>

                            <li>
                                <a href="#">Shop DC Collectibles</a>
                            </li>
                        </ul>
                    </nav>

                    <nav class="nav-center">
                        <h3>DC</h3>
                        <ul>
                            <li>
                                <a href="#">Terms Of Use</a>
                            </li>

                            <li>
                                <a href="#">Privacy policy (New)</a>
                            </li>

                            <li>
                                <a href="#">Ad Choices</a>
                            </li>

                            <li>
                                <a href="#">Advertising</a>
                            </li>

                            <li>
                                <a href="#">Jobs</a>
                            </li>

                            <li>
                                <a href="#">Subscriptions</a>
                            </li>

                            <li>
                                <a href="#">Talent Workshop</a>
                            </li>

                            <li>
                                <a href="#">CPSC Certificates</a>
                            </li>

                            <li>
                                <a href="#">Ratings</a>
                            </li>

                            <li>
                                <a href="#">Shop Help</a>
                            </li>

                            <li>
                                <a href="#">Contact Us</a>
                            </li>
                        </ul>
                    </nav>

                    <nav class="nav-right">
                        <h3>SITES</h3>
                        <ul>
                            <li>
                                <a href="#">DC</a>
                            </li>

                            <li>
                                <a href="#">MAD Magazine</a>
                            </li>

                            <li>
                                <a href="#">DC Kids</a>
                            </li>

                            <li>
                                <a href="#">DC Universe</a>
                            </li>

                            <li>
                                <a href="#">DC Power Visa</a>
                            </li>
                        </ul>
                    </nav>
                </div>
                <!-- /FOOTER TOP LEFT -->

                <!-- FOOTER TOP RIGHT -->
                <div class="footer-top-right"></div>
                <!-- /FOOTER TOP RIGHT -->
            </div>
        </div>
        <!-- /FOOTER TOP -->

        <div class="footer-bottom">
            <div class="container">
                <div class="footer-bottom-left">
                    <button class="btn"><a href="">SIGN-UP NOW!</a></button>
                </div>

                <div class="footer-bottom-right">
                    <h3>FOLLOW US</h3>
                    
                    <a href="">
                        <img src="../assets/img/footer-facebook.png" alt="Logo di Facebook">
                    </a>

                    <a href="">
                        <img src="../assets/img/footer-twitter.png" alt="Logo di Twitter">
                    </a>

                    <a href="">
                        <img src="../assets/img/footer-youtube.png" alt="Logo di YouTube">
                    </a>

                    <a href="">
                        <img src="../assets/img/footer-pinterest.png" alt="Logo di Pinterest">
                    </a>

                    <a href="">
                        <img src="../assets/img/footer-periscope.png" alt="Logo di Periscope">
                    </a>
                </div>
            </div>

            
        </div>
    </footer>
</template>

<style lang="scss" scoped>
@use '../styles/partials/mixins' as *;
@use '../styles/partials/variables' as *;

footer{
    .footer-top{
        width: 100%;
        background-image: url(../assets/img/footer-bg.jpg);
        background-size: cover;
        background-repeat: no-repeat;
        .container{
            @include flex-container(space-between);

            .footer-top-left{
                padding: 2rem 0;
                @include flex-container(space-between);
                gap: 2rem;

                nav{
                    h3{
                        color: white;
                        margin: 1rem 0;
                    }

                    ul{
                        li{
                            color: lighten($main-dark, 30%);
                            margin-bottom: .3rem;
                            a{
                                border-bottom: 1px solid transparent;

                                &:hover{
                                    border-bottom: 1px solid lighten($main-dark, 30%);
                                }
                            }
                        }
                    }
                }
            }

            .footer-top-right{
                width: 70%;
                background-image: url(../assets/img/dc-logo-bg.png);
                background-repeat: no-repeat;
                background-position: center right;
            }
        }
    }

    .footer-bottom{
        background-color: lighten($main-dark, 5%);
        padding: .8rem 0;

        .container{
            @include flex-container(space-between);
            align-items: center;
            .footer-bottom-left{
                .btn{
                    padding: .6rem;
                    background-color: transparent;
                    color: white;
                    border: 1px solid $main-blue;
                    transition: all 125ms linear;
                }

                &:hover{
                    background-color: lighten($main-dark, 10%);
                }
            }
        }

        .footer-bottom-right{
            @include flex-container(space-between);
            align-items: center;

            h3{
                font-size: .9rem;
                color: $main-blue;
                margin-right: .5rem;
            }

            img{
                width: 70%;
            }
        }
    }
}
</style>