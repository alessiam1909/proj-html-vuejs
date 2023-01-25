<script>
export default {
    props: {
        footerList: Array
    },  
}
</script>

<template lang="">
    <div class="container-footer1">
        <div class="row-footer">
            <div class="col col1">
                <img src="../assets/images/avada-drivers-logo-1x.png" alt="logo">
                <p>Avada Driving School is the right choice for experienced drivers looking for a refresher course, or the brand new driver wanting to pass first time.</p>
            </div>
            <div class="col col2">
                <h3>CONTACT DETAILS</h3>
                <div class="icone">
                    
                    <p> <i class="fa-solid fa-house"></i> 12345 North Main Street, New York, NY 555555</p>
                   
                    <p>  <i class="fa-solid fa-phone"></i>1.800.555.6789</p>
                    
                    <p><i class="fa-solid fa-envelope"></i>info@your-domain.com</p>
                    
                    <p><i class="fa-solid fa-link"></i>Theme-Fusion.com</p>
                </div>
            </div>
            <div class="col col3">
                <h3>COURSES</h3>
                <ul>
                    <li v-for="(item, index) in footerList" :key="index">
                        <i class="fa-solid fa-circle-arrow-right"></i>
                         <p>{{item.title}}</p>
                    </li>
                </ul>
            </div>
            <div class="col col4">
                <img src="../assets/imageS/footer-ad-grid-200x178.png" alt="img-footer">
                <button>BOOK NOW</button>
            </div>
        </div>
    </div>
    <div class="container-footer2">
        <div class="row-footer2">
            <div class="par">
                <p><i class="fa-regular fa-copyright"></i> Copyright 2012 - 2013 | Avada Theme by <a href="">ThemeFusion</a> | All Rights Reserved | Powered by <a href="">Wordpress</a></p>
            </div>
            <div class="icons">
                <i class="fa-brands fa-facebook-f"></i>
                <i class="fa-brands fa-twitter"></i>
                <i class="fa-brands fa-youtube"></i>
                <i class="fa-brands fa-instagram"></i>
    
            </div>
        </div>
    </div>
</template>

<style lang="scss">
     @use '../styles/partials/variables.scss' as *;
    @use '../styles/partials/mixins.scss' as *;

    .container-footer1{
        background-image: url('../assets/images/footer-background-color.jpg');
        height: 500px;
        background-size: cover;

        .row-footer{
            @include width70;
            @include flex-between;
            height: 100%;
            

            .col{
                width: calc(100% / 4);
                margin: 0 20px;
                

            }

            .col1{
                p{
                    color: $blue;
                    padding: 20px 0;
                }
            }

            .col2{
                color: $blue;
                h3{
                    margin-bottom: 10px;
                    color: $white;
                }

                .icone{
                    p{
                        padding: 10px 0;
                    }

                    i{
                        padding-right: 15px;
                    }
                }

                
            }

            .col3{
                h3{
                    color: $white;
                    margin-bottom: 20px;
                }

                ul{
                    list-style-type: none;

                    li{
                        display: flex;
                        padding: 10px 0;
                        color: $green;

                        i{
                            padding-right: 10px;
                        }
                    }
                }
            }

            .col4{
                display: flex;
                flex-direction: column;
                align-items: center;

                img{
                    width: 80%;
                }

                button{
                    width: 60%;
                    background-color: $green;
                    color: $white;
                    border: none;
                    padding: 10px 25px;
                    font-size: 15px;
                    border-radius: 20px;
                    font-weight: 500;
                    margin-top: 30px;
                    

                    &:hover, &:active{
                        background-color:  rgba(122, 188, 100, 0.75);
                        transition: all 0.5s;
                        cursor: pointer;
                    }
                }
            }
        }
    }

    .container-footer2{
        height: 100px;
        background-color: $black;

        .row-footer2{
            @include width70;
            @include flex-between;
            padding: 30px;
            height: 100%;

            .par{
                p{
                    color: $blue;
                    font-size: 13px;
                }

                a{
                    text-decoration: none;
                    color: $green;
                }
            }

            .icons{
                color: $white;
                
                i{
                    padding: 0 10px;
                }
            }
        }
    }
</style>