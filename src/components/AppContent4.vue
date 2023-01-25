<script>
export default {
    
}
</script>

<template lang="">
    <div class="container4">
        <img src="../assets/images/latestnews-bottom-800x70.png" alt="triangle">
        <div class="row">
            <div class="card-rate">
                <div class="circle"> 
                    <div class="inside-circle">
                            90%
                    </div>
                </div>
                <h3>PASS RATE</h3>
            </div>
            <div class="card-rate">
                <div class="circle"> 
                    <div class="inside-circle">
                            100%
                    </div>
                </div>
                <h3>REFERRAL RATE</h3>
            </div>
            <div class="card-rate">
                <div class="circle"> 
                    <div class="inside-circle">
                            0%
                    </div>
                </div>
                <h3>ACCIDENT RATE</h3>
            </div>
        </div>
    </div>
</template>

<style lang="scss">
    @use '../styles/partials/variables.scss' as *;
    @use '../styles/partials/mixins.scss' as *;

    .container4{
        position: relative;
        height: 400px;
        img{
            width: 100vw;
            filter: invert(5%)
        }

        .row{
            @include width70;
            @include flex-between;
            padding: 0 100px;
            position: absolute;
            padding-bottom: 100px;
            top: -10%;
            left: 15%;


            .card-rate{
                width: 30%;
                height: 400px;
                text-align: center;
                margin: 0 20px;
                border-radius: 10px;
                border-top: 7px solid $green;
                background-color: white;
                border-left: 1px solid $lightgrey;
                border-right: 1px solid $lightgrey;
                border-bottom: 1px solid $lightgrey;
                box-shadow: 5px 10px 10px 5px rgba(0, 0, 0, 0.1);
                

                .circle {
                    border: 15px solid $lightgrey;
                    border-top: 15px solid $green;
                    border-radius: 50%;
                    position: relative;
                    margin:50px  20%;
                    width: 200px;
                    height: 200px;
                    animation: spin 2s ease-in-out;

                     @keyframes spin {
                            0% { 
                                transform: rotate(0deg); 
                                
                            }
                            100% { 
                                transform: rotate(360deg); 
                                
                            }
                    }

                    .inside-circle{
                        margin: 20px;
                        position: absolute;
                        top: 25%;
                        left: 15%;
                        font-size: 40px;
                        color: $blue;
                    }
                    

                }

                h3{
                    color: $blue;
                }
            }
        }
    }
</style>