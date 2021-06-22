<template>
    <section>
        <div class="container">
            <div class="container-70">
                <div class="container-40">
                    <h3>
                        What we do?
                    </h3>
                    <p>
                        Lorem ipsum dolor sit amet consectetur adipisicing elit. Velit maxime et qui nemo sequi placeat sapiente amet ea.
                    </p>
                    <button>
                        Read more
                        <i class="fas fa-caret-right"></i>
                    </button>
                </div>

                <div class="container-60 ">
                    <div>
                        <img src="../assets/img/h2-icon-01.png" alt="tree">
                        <div>
                            Beautifull illustrations
                        </div>
                    </div>
                    <div>
                        <img src="../assets/img/h2-icon-02.png" alt="bush">
                        <div>
                            Brand Strategies
                        </div> 
                    </div>
                    <div>
                        <img src="../assets/img/h2-icon-03.png" alt="umbrella">
                        <div>
                            Qualified support
                        </div>
                    </div>
                    <div>
                        <img src="../assets/img/h2-icon-04.png" alt="books">
                        <div>
                            Books & magazines
                        </div>
                    </div>
                </div>
                
            </div>
            <div class="social-media">

                <a href="#"><i class="fab fa-instagram"></i></a>
                <a href="#"><i class="fab fa-facebook-f"></i></a>
                <a href="#"><i class="fab fa-twitter"></i></a>
                <a href="#"><i class="fab fa-pinterest-p"></i></a>
                
            </div>
        <div class="video-player">
            <img src="../assets/img/main-home-video-button-img-01.png" alt="green-player" class="green-player">
            <img src="../assets/img/main-home-video-button-img-02.png" alt="red-player" class="red-player">
        </div>
        </div>
    </section>
</template>
            
            
            


<script>
export default {
    name: "WhatWeDo",
}
</script>

<style lang="scss" scoped>
    @import "../style/variables.scss";

    .container {
        position: relative;
    }

    .container-70 {
        display: flex;
        margin-top: 70px;
        max-width: 691px;
    }

    .container-40 {
        h3 {
            font-size: 26px;
            color: $mainTextColor4;
        }

        p {
            margin: 15px 0;
            font-size: 12px;
            color: $mainTextColor2;
        }

        button {
            background-color: $bgMainColor1;
            padding: 5px 25px;
            border: 2px solid #80ABAE;
            border-radius: 15px;
            font-size: 12px;
            font-weight: bold;
            color: $mainTextColor4;
            cursor: pointer;

            i {
                font-size: 10px;
                margin-left: 5px;
            }
        }

        button:hover {
            background-color: #80ABAE;
            color: $bgMainColor1;
        }
    }

    .container-60 {
        display: flex;
        flex-wrap: wrap;

        div {
            width: 50%;
            display: flex;
            justify-content: center;
            align-items: center;
            padding-left: 20px;

            img {
                height: 60%;
            }

            div {
                padding-left: 20px;
                font-size: 14px;
                font-weight: bold;
                color: $mainTextColor4;
            }
        }

        & > div:hover {
            border: 1px solid #EFCA9E;
            border-radius: 20px;
            cursor: pointer;
        }
    }

    .social-media {
        position: absolute;
        top: 0px;
        right: 10px;
        display: flex;
        flex-direction: column;

        i {
            margin: 10px 0;
            font-size: 12px;
            color: black;
        }
    }

    .video-player {
        margin: 50px 0;
        width: 100%;
        height: 500px;
        background-image: url("../assets/img/h2-img-2.jpg");
        background-size: cover;
        display: flex;
        justify-content: center;
        align-items: center;
        cursor: pointer;

        img {
            cursor: pointer;
        }

        .red-player {
            display: none;
        }
    }

    .video-player:hover {

        .green-player {
            display: none;
        }

        .red-player {
            display: inline-block;
        }
    }

        

</style>