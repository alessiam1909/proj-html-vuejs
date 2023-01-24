<script>
export default {
    props: {
        navList: Array
    },
    methods: {
        newSection(){

        }
    }
}
</script>

<template lang="">
    <div class="first-header">
        <div class="row">
            <div>We have a 95% Successful Pass Rate!</div>
            <div><i class="fa-solid fa-phone"></i>Give us a call to book your tuition! 1-800-555-555</div>
        </div>
        <div class="jumbo">
            <div class="bg-header">
                <header>
                    <img src="../assets/images/avada-drivers-logo-1x.png" alt="logo">
                    <ul class="navbar">
                        <li v-for="(item, index) in navList" :key="index">
                            <div>
                                <a :href="item.url">{{item.name}}</a>
                                <span v-if="item.new" class="newButton">NEW</span> 
                                <i v-if="item.new" class="fa-solid fa-chevron-down"></i>
                                <ul v-if="item.dropdownMenu" class="dropdown">
                                    <li v-for="(item, index) in item.dropdownMenu" :key="index">
                                        <a href="">{{item}}</a>
                                    </li>
                                </ul>
                            </div>
                        </li>
                    </ul>
                    <button>BOOK NOW</button>
                </header>
            </div>
            <div class="titolo">
                <h1>Drive with Avada</h1>
                <p>We offer the finest driving tuition money can buy</p>
            </div>
        </div>
    </div>
</template>

<style lang="scss">
    @use '../styles/partials/variables.scss' as *;
    @use '../styles/partials/mixins.scss' as *;


    .first-header{
        background-color: $black;
        width: 100%;
        height: 50px;

        .row{
            @include width70;
            @include flex-between;
            color: #6f879e;
            height: 100%;
            font-size: 15px;

            i{
                margin-right: 10px;
            }
        }

        .jumbo{
            background-image: url('../assets/images/homepage-hero-background.jpg') ;
            background-size: cover;
            height: 650px;
            width: 100%;
            background-repeat: no-repeat;

            .bg-header{
                background-color: rgba(73, 76, 78, 0.5);
                height:120px;

                header{
                    @include width70;
                    @include flex-between;
                    height: 100%;
                    
                    .navbar{
                        list-style-type: none;
                        display: flex;
                        position: relative;
                        
                        li{
                            margin: 0 20px;
                            padding: 12px;
                            font-size: 17px;

                            a{
                                text-decoration: none;
                                color: $white;
                            }
    
                            span{
                                color: $white;
                                padding: 5px;
                                margin: 0 10px;
                                background-color: $green;
                                font-size: 15px;
                                border-radius: 5px;
                            }

                            i{
                                color: $white;
                                font-size: 12px;
                                padding: 2px;
                            }
    
                            .dropdown{
                                display: none;
                                position: absolute;
                                background-color:$white ;
                                color: black;



                            }

                        }

                    }

                    button{
                        background-color: $green;
                        color: $white;
                        border: none;
                        padding: 10px 25px;
                        font-size: 17px;
                        border-radius: 20px;
                        
                    }
                }
            }

            .titolo{
                color: $white;
                @include width70;
                font-size: 28px;
                margin-top: 10%;
            }
        }
    }
</style>