<script>
export default {
    
}
</script>

<template lang="">
    <div class="container7">
        <div class="ctn-cards">
            <div class="news">
                <h1>Latest News</h1>
                <div class="row-news">
                    <div class="card-news">
                        <div class="ctn-news">
                            <img src="../assets/images/blog-choosecar-320x202.jpg" alt="car">
                        </div>
                        <h3>What Car to Start With?</h3>
                        <p class="data">February 7th, 2019 | <a href="#">0 Comments</a></p>
                        <p>Lorem ipsum dolor sit amet, consectetur adipiscing</p>
                    </div>
                    <div class="card-news">
                        <div class="ctn-news">
                            <img src="../assets/images/blogpost-10and2-320x202.jpg" alt="car">
                        </div>
                        <h3>Avada Driving School Expanding</h3>
                        <p class="data">February 7th, 2019 | <a href="#">0 Comments</a></p>
                        <p>Lorem ipsum dolor sit amet, consectetur adipiscing</p>
                    </div>
                </div>
                <button><a href="">MORE FROM THE BLOG</a></button>
            </div>
            <img src="../assets/images/latestnews-bottom-1200x105.png" alt="triangle">
        </div>
    
    </div>
    <div class="container8">
        <div class="row-subfooter">
            <h1>Sign Up to our Newsletter</h1>
            <input type="text">
            <button>SUBSCRIBE</button>
            <p>(We do not share your data with anybody, and only use it for its intended purpose)</p>
        </div>
    </div>
</template>

<style lang="scss">
     @use '../styles/partials/variables.scss' as *;
    @use '../styles/partials/mixins.scss' as *;

    .container7{
        background-image: url('../assets/images/latestnews-background.jpg');
        height: 700px;
        background-size: cover;
        position: relative;
        background-position: bottom left;

        .ctn-cards{
            width: 62.5%;
            top: -20px;
            left: 19%;
            position: absolute;
            border-top-right-radius: 15px;
            border-top-left-radius: 15px;
            border-top: 5px solid $grey;
            margin: 0 auto;
            

            .news{
                border-top-right-radius: 15px;
                border-top-left-radius: 15px;
                background-color: $white;
                text-align: center;

                h1{
                    color: $black;
                    padding: 30px 0;
                }

                .row-news{
                    display: flex;
                    width: 90%;
                    margin: 0 auto;

                    .card-news{
                        width: calc(100% / 2);
                        margin: 0 20px;
                        .ctn-news{
                            width: 100%;
                            height: 300px;
                            overflow: hidden;
                            img{
                                width: 100%;
                                height: 100%;
                                transition: transform 1s ease;
    
                                &:hover{
                                    transform: scale(1.2);
                                }
                            }
                        }

                        h3{
                            padding: 10px 0 5px;
                            color: $green;
                        }

                        p{
                            color: $blue;
                            padding-bottom: 10px;
                        }

                        .data{
                            font-size: 12px;

                            a{
                                text-decoration: none;
                                color: $green;
                            }
                        }
                    }
                }

                button{
                    margin-top: 20px;
                    padding: 10px;
                    background-color: $green;
                    border: none;
                    border-radius: 20px;

                    a{
                        text-decoration: none;
                        color: white;
                        font-weight: 600;
                        padding: 10px 15px;
                    }
                    &:hover{
                        background-color:  rgba(108, 158, 91);
                        transition: all 0.5s;
                        cursor: pointer;
                    }
                }
            }

            

        }
    }

    .container8{
        background-image: url('../assets/images/newsletter_background.jpg');
        background-size: cover;
        background-position:top left;
        height: 300px;
        position: relative;
        text-align: center;

        .row-subfooter{
            display: flex;
            flex-direction: column;
            width: 30%;
            margin: 0 auto;

            h1{
                color: $black;
                padding: 20px 0;
            }

            input{
                height: 40px;
                margin-bottom: 30px;
            }

            button{
                height: 40px;
                background-color: $green;
                color: $white;
                border: none;
                border-radius: 20px;
                font-weight: 600;

                &:hover{
                        background-color:  rgba(108, 158, 91);
                        transition: all 0.5s;
                        cursor: pointer;
                    }
            }

            p{
                padding-top: 30px;
                color: $blue;
            }
        }
    }
</style>