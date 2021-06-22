<template>
    <section>
        <div class="first-block">
            <div class="container-70 pricing">
                <div>
                    <h4>Basic</h4>
                    <h3>
                        99
                        <span>$</span>
                    </h3>
                    <ul>
                        <li>5 Design concepts</li>
                        <li>Full copyright ownership</li>
                        <li>Art direction</li>
                        <li>Top level creatives</li>
                        <li>No money back</li>
                    </ul>
                    <button class="btn">
                        Read more
                        <i class="fas fa-caret-right"></i>
                    </button>
                </div>
                <div>
                    <h4>Standard</h4>
                    <h3>
                        119
                        <span>$</span>
                    </h3>
                    <ul>
                        <li>10 Design concepts</li>
                        <li>Full copyright ownership</li>
                        <li>Art direction</li>
                        <li>Top level creatives</li>
                        <li>No money back</li>
                    </ul>
                    <button class="btn">
                        Read more
                        <i class="fas fa-caret-right"></i>
                    </button>
                </div>
                <div>
                    <h4>Premium</h4>
                    <h3>
                        139
                        <span>$</span>
                    </h3>
                    <ul>
                        <li>15 Design concepts</li>
                        <li>Full copyright ownership</li>
                        <li>Art direction</li>
                        <li>Top level creatives</li>
                        <li>No money back</li>
                    </ul>
                    <button class="btn">
                        Read more
                        <i class="fas fa-caret-right"></i>
                    </button>
                </div>
            </div>
            <div class="asides">
                <div>
                    <img src="../assets/svg/svg-2.svg" alt="">
                </div>
                <div>
                    <img src="../assets/svg/svg-4.svg" alt="">
                </div>
            </div>
        </div>
        
        <div class="second-block">
            <div class="container-70" id="getInTouch">
                <div>
                    <h3>
                        Get in touch and say hello
                    </h3>
                    <p>
                        Lorem ipsum dolor sit amet consectetur adipisicing elit. Molestias quos quidem iure, officiis aspernatur ex.
                    </p>
                </div>
                <div>
                    <form>
                        <input type="text" placeholder="Comment" class="comment">
                        <input type="text" placeholder="Name" class="name">
                        <input type="text" placeholder="Email" class="email">
                        <button class="btn">
                            Submit
                            <i class="fas fa-caret-right"></i>
                        </button>
                    </form>
                </div>
            </div>
        </div>
    </section>
</template>

<script>
export default {
    name: "LearnMore",
}
</script>

<style lang="scss" scoped>
@import "../style/variables.scss";

    .first-block {
        position: relative;
        background-image: url("../assets/img/h2-background-img-03.png");
        background-size: contain;
    }

    .pricing {
        display: flex;
        justify-content: space-between;

        div {
            display:flex;
            flex-direction: column;
            align-items: center;
            width: 30%;
            margin: 70px 0;
            padding: 40px 30px;
            // height: 400px;
            border-radius: 15px;
            color: $mainTextColor4;
            border: 2px solid #EFCA9E;
            cursor: pointer;
            transition: all 0.5s;

            h3 {
                position: relative;
                font-size: 36px;
                margin: 20px 0;

                span {
                    position: absolute;
                    top: 5px;
                    right: -10px;
                    font-size: 14px;
                }
            }

            ul {
                list-style: none;
                text-align: center;
                margin-bottom: 20px;

                li {
                    font-size: 12px;
                    color: $mainTextColor1;
                    padding: 5px;
                }
            }

            .btn:hover {
                background-color: #80ABAE;
                color: white;
                transform: scale(1.1);
            }
        }
        div:hover {
            transform: scale(1.1);  
        }

        div:nth-child(2) {
           background-color: #E6F3F0; 
           border: none;

            .btn {
               background-color: #E6F3F0;
               
            }

            .btn:hover {
                background-color: #80ABAE;
                transform: scale(1.1); 
            }
        }

        div:last-child {
            border: 2px solid #EA9B82;
        }
    }

    .asides {
        position: absolute;
        top: 50%;
        right: 0;
        cursor: pointer;
        transition: all 1s;

        div {
            width: 50px;
            height: 50px;

            img {
                width: 100%;
                padding: 10px;
            }
        }

        div:first-child {
            background-color: #EF2853;
        }

        div:last-child {
            margin-top: 5px;
            background-color: white;
        }

        div:hover {
            transform: scale(1.1);  
        }
    }




    #getInTouch {
        display: flex;
        margin: 70px auto;

        div {
            width: 50%;
        }

        div:first-child {
            padding-right: 90px;

            h3 {
                font-size: 36px;
                padding-right: 80px;
                color: $mainTextColor4;
            }

            p {
                margin: 10px 0;
                font-size: 12px;
                color: $mainTextColor1;
            }
        }

        form {

            input {
                border: none;
                border-bottom: 1px solid $mainTextColor4;
                color: $mainTextColor1 ;
                padding: 5px 0;
            }

            .comment {
                display: inline-block;
                width: 100%;
            }

            .name,
            .email {
                width: calc(50% - 10px);
                margin: 30px 0;
            }

            .name {
                margin-right: 20px;
            }

            .btn:hover {
            background-color: #80ABAE;
            color: white;
            transform: scale(1.1);
            }

        }
    }
</style>