<script>
export default {
    
}
</script>

<template lang="">
    <div class="container3">
        <div class="row">
            <div class="corsi">
                <div class="title-corsi">
                    <img src="../assets/images/new-corner.jpg" alt="new">
                    <h1>Courses</h1>
                </div>
                <p>Lorem ipsum, dolor sit amet consectetur adipisicing elit. Laborum nihil temporibus, veritatis nobis similique sed, modi vel enim fuga ullam et maiores! Quidem a
                quas.</p>
                <button>
                    <a href="#">COURSE INFORMATION</a>
                </button>
            </div>
            <div class="tipi">
                <div class="card">
                    <div class="ctn-img">
                        <img src="../assets/images/courses-passplus-200x200.jpg" alt="img1">
                    </div>
                    <h3>Pass Plus</h3>
                    <button > <a href="https://avada.theme-fusion.com/driving/courses/intensive-driving-course/"> LEARN MORE</a></button>
                </div>
                <div class="card">
                    <div class="ctn-img">
                        <img src="../assets/images/course-intensive-200x200.jpg" alt="img2">
                    </div>
                    <h3>Intensive Course</h3>
                    <button> <a href="https://avada.theme-fusion.com/driving/courses/intensive-driving-course/"> LEARN MORE</a></button>
                </div>
                <div class="card">
                    <div class="ctn-img">
                        <img src="../assets/images/courses-instructor-200x200.jpg" alt="img3">
                    </div>
                    <h3>Instructors</h3>
                    <button> <a href="https://avada.theme-fusion.com/driving/courses/intensive-driving-course/"> LEARN MORE</a></button>
                </div>
                
            </div>
        </div>
    </div>
</template>

<style lang="scss">
    @use '../styles/partials/variables.scss' as *;
    @use '../styles/partials/mixins.scss' as *;

    .container3{
        background-image: url('../assets/images/promise-background.jpg');
        background-size: cover;
        background-position: left bottom;
        height: 500px;
        position: relative;

        .row{
            @include width70;
            @include flex-between;

            .corsi{
                width: 23%;
                background-color: $white;
                text-align: center;
                height: 400px;
                border-radius: 15px;
                position: absolute;
                top: -30px;
                box-shadow: 5px 10px 10px 5px rgba(0, 0, 0, 0.1);

                .title-corsi{
                    display: flex;
                    align-items: baseline;
                    text-align: center;

                    img{
                        border-top-left-radius: 15px;
                        width: 80px;
                        height: 80px
                    };

                    h1{
                        margin:20px 40px;
                        color: $black;
                        padding-left: 20px;
                        font-size: 40px;

                    }
                }

                p{
                    font-size: 15px;
                    color: $blue;
                    margin: 0 40px;
                    line-height: 25px;
                }

                button{
                    margin: 40px;
                    background-color: $green;
                    padding: 15px;
                    border: none;
                    border-radius: 20px;

                    a{
                        text-decoration: none;
                        color: $white;
                        font-size: 15px;
                        font-weight: 600;
                    }

                    &:hover{
                        background-color:  rgba(108, 158, 91);
                        transition: all 0.5s;
                        cursor: pointer;
                    }
                }
            }

            .tipi{
                width: 50%;
                display: flex;
                position: absolute;
                top: 100px;
                left: 43%;

                .card{
                    width: 200px;
                    margin: 0 20px;
                    text-align: center;

                    .ctn-img{
                        width: 100%;
                        height: 200px;
                        overflow: hidden;

                        img{
                            width: 100%;
                            transition: transform 1s ease;

                            &:hover{
                                transform: scale(1.2);
                            }
                        }
                    }

                    h3{
                        color: $grey;
                        margin: 20px 0;
                        font-size: 20px;
                    }

                    button{
                        border: 3px solid $grey;
                        border-radius: 20px;
                        padding: 10px;

                        a{
                            text-decoration: none;
                            color: $grey;
                            font-weight: 600;
                            padding: 10px;
                            

                            &:hover{
                                color: $green;
                            }
                        }

                        &:hover, &:active{
                            border: 3px solid $green;
                            background-color: $lightgrey;
                        }
                    }
                }
            }
        }
    }
</style>