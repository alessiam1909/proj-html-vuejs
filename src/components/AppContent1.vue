<script>
export default {
    
}
</script>
<template lang="">
    <div class="container">
        <div class="paragrafo">
            <h1>Get Behind The Wheel</h1>
            <p class="sub">Lorem ipsum dolor sit, amet consectetur adipisicing elit. Vero quibusdam molestias laudantium, maxime voluptate optio quasi ipsam ad, dignissimos id animi.</p>
            <p class="small">Lorem ipsum dolor, sit amet consectetur adipisicing elit. Laudantium in quas perferendis, dolores aliquam error enim earum, voluptas ea recusandae ipsa quod, laborum exercitationem voluptates rerum suscipit sapiente. Eum, aliquid. Lorem ipsum dolor, sit amet consectetur adipisicing elit. .</p>
        </div>
        <div class="form">
            <h2>First Lesson Free!</h2>
            <p>When you make a block booking with us your first lesson is included free.</p>
            <input type="text" name="" id="" placeholder="Your Name*" required>
            <input type="email" name="" id="" placeholder="Email*" required>
            <input type="text" name="" id="" placeholder="Telephone" >
            <input type="text" name="" id="" placeholder="Location" >
        </div>
    </div>
</template>

<style lang="scss">
    @use '../styles/partials/variables.scss' as *;
    @use '../styles/partials/mixins.scss' as *;

    .container{
        @include width70;
        @include flex-between;

        .paragrafo{
            width: 40%;
            margin: 50px;

            h1{
                color: $black;
                margin: 30px 0;
                font-size: 35px;
            }

            p{
                color: $blue;
                margin: 20px 0;
            }

            .sub{
                font-size: 23px;
            }

            .small{
                font-size: 17px;
            }
        }

        .form{
            position: absolute;
            border-radius: 20px;
            border: 1px solid $lightgrey;
            left: 50%;
            top: 70%;
            height: 600px;
            background-color: $white;
            text-align: center;
            width: 27%;
            box-shadow: 5px 10px 10px 5px $lightgrey;

            h2{
                color: $green;
                font-size: 30px;
                margin: 30px 0;
            }

            p{
                color: $blue;
                font-size: 15px;
                margin: 0 35px;
            }

            input{
                display: block;
                width: 80%;
                margin: 40px auto ;
                height: 50px;
                background-color: $lightgrey;
                border: 1px solid $grey;
                padding-left: 20px;

                &:active, &:focus{
                    outline: none;
                   
                }
            }
        }
    }
</style>