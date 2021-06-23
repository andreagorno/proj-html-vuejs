<template>

    <div class="main">
        <div class="container">
            
            <!-- company-info start -->
            <div class="company-info">
                <div>
                    <h2>We are Bryson, New York-based art & design studio</h2>
                </div>
                <div>
                    <p>
                        Here at Bryson it only taken smidgen of imagination and we're already prepared ourselves for future challenges. Take a peek and see if you recognize the trademark ingredients of our work.
                    </p>
                </div>
            </div>
            <!-- /company-info start -->

        </div>
            <!-- jumbotron and labels start -->
            <div class="jumbotron container-70">
               <div 
               v-for="(item, index) in items"
               :key="index"
               class="cube">
                    <img 
                    :src="require(`@/assets/img/${item.poster}`)" 
                    :alt="item.h4">
                    <div class="label">
                        <div>
                            <h4> {{ item.h4 }} </h4>
                            <h5> {{ item.h5 }} </h5>
                       </div>
                    </div>
                </div>  
            </div>
            <!-- jumbotron and labels start -->
    
    </div>
    
</template>

<script>
export default {
    name: "PageIntro",

    props: {
        items: [ Array ]
    },
    
}
</script>

<style lang="scss" scoped>
@import "../style/variables.scss";

    .main {
        background-image: url("../assets/img/h2-background-img-02.png"), url("../assets/img/h2-background-img-01.png");
        background-size: 90%;
        background-repeat: repeat-x;
        background-position-y: 0%, 90%;
        background-position-x: 0px, -65px;
        max-width: 1700px;
        margin: auto;
    }


    .company-info {
        display: flex;
        align-items: center;
        margin: 0 40px;

        div {
            width: 50%;
            margin-top: 50px;
        }

        h2 {
            font-size: 40px;
            margin: 40px 40px 40px 20px;
            padding-right: 50px;
            color: $mainTextColor3;
        }

        p {
            font-size: 14px;
            margin-left: 30px;
            color: $mainTextColor2;
        }
    }

    .jumbotron {
        display: flex;
        flex-wrap: wrap;
        margin: auto;
        margin-top: 50px;

        .cube {
            position: relative;
            width: 50%;

            img {
                width: 100%;
                height: 100%;
            }


            .label {
                display: none;
                flex-direction: column;
                justify-content: center;
                align-items: center;
                position: absolute;
                top: 0;
                left: 0;
                width: 130px;
                height: 130px;
                background: linear-gradient(135deg, white 50%, #F7BCA8 50%);

                div {
                    margin-top: 40px;
                    margin-left: 30px;
                    text-align: center;
                    transform: rotate(-45deg);
                    
                    h4 {
                        font-size: 14px;
                        color: $mainTextColor4;
                    }
                    h5 {
                        font-size: 12px;
                        color: $mainTextColor1;
                        font-weight: 400;
                    }
                    
                    
                }
            }
        }

        .cube:hover .label {
            display: flex;
        }
    }
</style>