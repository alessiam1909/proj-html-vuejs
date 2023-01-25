<script>
export default {
   data(){
    return{
        activeItem: 0,
        testimonials:[
           
            {
                img: '../assets/images/testimonial-grant.png',
                nome: 'Grant'
            },
            {
                img: '../assets/images/testimonial-harold.png',
                nome: 'Harold'
            },
            {
                img: '../assets/images/testimonial-kate.png',
                nome: 'Kate'
            },
            {
                img: '../assets/images/testimonial-kelly.png',
                nome: 'Kelly'
            },
            {
                img: '../assets/images/testimonial-sophia.png',
                nome: 'Sophia'
            },
        
        ]
    }
   }
}
</script>

<template lang="">
    <div class="container5">
        <h1>Your Instructors</h1>
        <div class="row">
            <h3>Lorem, ipsum dolor sit amet consectetur adipisicing elit. Aliquam facere perferendis molestiae laudantium rem consequatur nisi ipsum, itaque laboriosam expedita animi harum? Voluptate nulla in aut animi facere at saepe.</h3>
            <button><a href="">MORE ABOUT US</a></button>
        </div>
        <div class="row2">
            <div class="card">
                <div class="img-ctn">
                    <img src="../assets/images/instructor-mikehart-200x127.jpg" alt="ins1">
                </div>
                <h2>Mike Hart</h2>
                <div>
                    <i class="fa-brands fa-facebook-f"></i>
                    <i class="fa-brands fa-twitter"></i>
                    <i class="fa-brands fa-instagram"></i>
                </div>
                <p>Lorem ipsum dolor sit, amet consectetur adipisicing elit. Ullam officia natus, illum laboriosam at iure repellat animi ab quae ipsam iusto totam inventore voluptate    culpa esse. Aliquam alias numquam nostrum.</p>
            </div>
            <div class="card card2">
                <div class="img-ctn">
                    <img src="../assets/images/instructor-johnsmith-200x127.jpg" alt="ins1">
                </div>
                <h2>John Smith</h2>
                <div>
                    <i class="fa-brands fa-facebook-f"></i>
                    <i class="fa-brands fa-twitter"></i>
                    <i class="fa-brands fa-instagram"></i>
                </div>
                <p>Lorem ipsum dolor sit, amet consectetur adipisicing elit. Ullam officia natus, illum laboriosam at iure repellat animi ab quae ipsam iusto totam inventore voluptate    culpa esse. Aliquam alias numquam nostrum.</p>
            </div>
            <div class="card">
                <div class="img-ctn">
                    <img src="../assets/images/instructor-angelahart-200x127.jpg" alt="ins1">
                </div>
                <h2>Angela Hart</h2>
                <div>
                    <i class="fa-brands fa-facebook-f"></i>
                    <i class="fa-brands fa-twitter"></i>
                    <i class="fa-brands fa-instagram"></i>
                </div>
                <p>Lorem ipsum dolor sit, amet consectetur adipisicing elit. Ullam officia natus, illum laboriosam at iure repellat animi ab quae ipsam iusto totam inventore voluptate    culpa esse. Aliquam alias numquam nostrum.</p>
            </div>
        </div>
    </div>
    <div class="container6">
        <div class="width50">
            <h1>Testimonials</h1>
            <h2>Here's what our happy drivers had to say about our services:</h2>
            <div class="img-container">
                <img src="../assets/images/testimonial-grant.png" alt="tsm-img">
            </div>
            <p>Avada Driving School really helped build my confidence behind the wheel and with driving in general, and they got me a first time pass! Highly recommended.</p>
            <p class="name">Grant</p>
            <div class="circles-container">
                    <div class="circle"></div>
                    <div class="circle"></div>
                    <div class="circle"></div>
                    <div class="circle"></div>
                    <div class="circle"></div>
            </div>
        </div>
    </div>
</template>

<style lang="scss">
     @use '../styles/partials/variables.scss' as *;
    @use '../styles/partials/mixins.scss' as *;

    .container5{
        width: 60%;
        height: 600px;
        margin: 0 auto;
        color: $blue;
        padding-top: 50px;
        position: relative;
        
        h1{
            color: $black;
            margin-bottom: 50px
        }
        .row{
            @include flex-between;
            h3{
                width: 65%;
            }

            button{
                border: none;
                background-color: $green;
                margin-right: 100px;
                padding: 10px 20px;
                border-radius: 20px;

                a{
                    text-decoration: none;
                    color: white;
                    padding: 0 20px;
                    font-weight: 600;
                    font-size: 15px;
                }

                &:hover{
                        background-color:  rgba(108, 158, 91);
                        transition: all 0.5s;
                        cursor: pointer;
                }
            }
        }

        .row2{
            margin: 50px 0;
            display: flex;
            justify-content: space-between;
            position: absolute;
            z-index: 1;

            .card{
                padding: 30px ;
                width: 33%;
                height: 420px;
                text-align: center;
                margin: 0 10px;
                border-radius: 10px;
                border-top: 7px solid $green;
                background-color: white;
                border-left: 1px solid $lightgrey;
                border-right: 1px solid $lightgrey;
                border-bottom: 1px solid $lightgrey;
                box-shadow: 5px 10px 10px 5px rgba(0, 0, 0, 0.1);

                img{
                    width: 80%;
                    transition: all 1s ease;

                    &:hover{
                        transform: scale(1.1);
                        box-shadow:  5px 10px 10px 5px rgba(0, 0, 0, 0.1);
                    }
                }

                h2{
                    margin: 10px;
                }

                i{
                    padding: 10px;
                }

                p{
                    font-size: 15px;
                }
            }

            .card2{
                height: 440px;
            }
        }
    }

    .container6{
        background-image: url('../assets/images/testimonial-background.jpg');
        height: 800px;
        padding-top: 200px;
        background-size: cover;
        position: relative;
        text-align: center;

        .width50{
            width: 50%;
            margin: 0 auto;

            h1{
                color: $black;
            }

            h2{
                color: $blue;
                margin: 20px;
            }

            .img-container{
                width: 200px;
                height: 200px;
                margin: 50px auto;
                img{
                    width: 100%;
                }
            }

            p{
                color: $blue;
                margin: 20px 100px;
                font-size: 20px;
            }

            .name{
                font-weight: 600;
            }

            .circles-container{
                display: flex;
                justify-content: center;
                .circle{
                    display: inline-block;
                    width: 10px;
                    height: 10px;
                    border-radius: 50%;
                    background-color: rgba(174, 174, 174, 0.509);
                    margin: 10px;
                    cursor: pointer;
                }
                
                
                .circle.active, .circle:hover{
                    background-color: rgba(174, 174, 174, 1); 
                }
            }


        }
    }
</style>