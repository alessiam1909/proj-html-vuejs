<script>
export default {
    props: {
        navList: Array
    },
    data(){
        return{
            activeItem: 0,
        }
    },
    methods:{
        changeItem(index){
            this.activeItem = index
        },
    }
}
</script>

<template lang="">
    <div class="first-header">
        <div class="row">
            <div>We have a 95% Successful Pass Rate!</div>
            <div><i class="fa-solid fa-phone"></i>Give us a call to book your tuition! 1-800-555-555</div>
        </div>
    </div>
    <div class="jumbo">
        <div class="bg-header">
            <header>
                <div>
                    <img src="../assets/images/avada-drivers-logo-1x.png" alt="logo">
                </div>
                <div class="nav">
                    <ul class="navbar">
                        <li v-for="(item, index) in navList" :key="index" class="list-item"  @click="changeItem(index)" > 
                            <div  @click="item.isOpen = !item.isOpen">
                                <a :href="item.url"  :class="(activeItem === index) ? 'active' : '' ">{{item.name}}</a>
                                <span v-if="item.new" class="newButton">NEW</span> 
                                <i v-if="item.new" class="fa-solid fa-chevron-down"></i>
                                <div v-if="item.isOpen">
                                    <ul v-if="item.dropdownMenu" class="dropdown">
                                        <li v-for="(item, index) in item.dropdownMenu" :key="index" >
                                            <a href="">{{item}}</a>
                                        </li>
                                    </ul>
                                </div>
                            </div>
                        </li>
                    </ul>
                    <button>BOOK NOW</button>
                </div>
            </header>
        </div>
        <div class="titolo">
            <h1>Drive with Avada</h1>
            <p>We offer the finest driving tuition money can buy</p>
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

    }
    .jumbo{
        background-image: url('../assets/images/homepage-hero-background.jpg') ;
        background-size: cover;
        height: 650px;
        width: 100%;
        position: relative;
        background-repeat: no-repeat;

        .bg-header{
            background-color: rgba(73, 76, 78, 0.5);
            height:120px;

            header{
                @include width70;
                @include flex-between;
                height: 100%;

                .nav{
                    width: 90%;
                    display: flex;
                    align-items: center;
                    justify-content: flex-end;
                }
                
                .navbar{
                    list-style-type: none;
                    display: flex;
                    position: relative;
                    margin-right: 40px;
                    
                    .list-item{
                        padding: 15px 0;
                        margin: 10px;
                        font-size: 15px;
                        border: none;
                        position: relative;

                        a{
                            
                            text-decoration: none;
                            color: $white;
                            padding: 10px; 

                            &:hover, &:active{
                            color: $green;
                            }
                            .active:hover, .active:active{
                            color: $green;
                            }
                        }
                        span{
                            color: $white;
                            padding: 3px;
                            background-color: $green;
                            font-size: 12px;
                            border-radius: 5px;
                        }

                        i{
                            color: $white;
                            margin-left: 5px;
                            font-size: 12px;
                            padding: 2px;

                            &:hover, &:active{
                            color: $green;
                        }
                        }

                        .dropdown{
                            position: absolute;
                            top: 65px;
                            left: 30%;
                            background-color:$white ;
                            list-style-type: none;
                            
                            li{
                                padding: 10px;
                                width: 100%;
                                height: 50px;
                                border-bottom: 1px solid $grey;
                                a{
                                    text-decoration: none;
                                    color: black;
                                    padding: 10px;
                                    &:hover, &:active{
                                        color: white;
                                        transition: all 1s;
                                    }

                                }
                                &:hover, &:active{
                                    background-color: $green;
                                    transition: all 1s;
                                }

                            }
                        }

                        &::after{
                            content: '';
                            position: absolute;
                            width: 0px;
                            height: 3px;
                            left: 50%;
                            bottom:0;
                            background-color: $green;
                            transition: all ease-in-out 0.5s;
                        }

                        &:hover::after{
                            width: 100%;
                            left: 0;
                        }

                        

                    }

                }

                button{
                    background-color: $green;
                    color: $white;
                    border: none;
                    padding: 10px 25px;
                    font-size: 15px;
                    border-radius: 20px;
                    

                    &:hover, &:active{
                        background-color:  rgba(122, 188, 100, 0.75);
                        transition: all 0.5s;
                        cursor: pointer;
                    }
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
</style>