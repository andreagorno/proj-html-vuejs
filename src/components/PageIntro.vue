<template>

    <div class="main">
        <div class="container">

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

            <div class="jumbotron">
               <div class="cube">
                    <img src="../assets/img/port-img-07.jpg" alt="">
                </div> 
               <div class="cube">
                   <img src="../assets/img/port-img-08.jpg" alt="">
                </div> 
               <div class="cube">
                    <img src="../assets/img/port-img-09.jpg" alt="">   
                </div> 
                <div class="cube">
                    <img src="../assets/img/port-img-10.jpg" alt="">
                </div> 
               <div class="cube">
                    <img src="../assets/img/port-img-11.jpg" alt="">   
                </div> 
               <div class="cube">
                    <img src="../assets/img/port-img-12.jpg" alt="">   
                </div> 
            </div>
            
        </div>
    </div>
    
</template>

<script>
export default {
    name: "PageIntro"
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
        max-width: 1235px;
        margin: auto;
    }


    .company-info {
        display: flex;
        align-items: center;

        div {
            width: 50%;
        }

        h2 {
            font-size: 42px;
            margin: 40px 40px 40px 20px;
            color: $mainTextColor3;
        }

        p {
            font-size: 14px;
            margin-left: 50px;
            color: $mainTextColor2;
        }
    }

    .jumbotron {
        display: flex;
        flex-wrap: wrap;
        width: 70%;
        margin: auto;
        margin-top: 50px;

        .cube {
            width: 50%;

            img {
                width: 100%;
                height: 100%;
            }
        }
    }
</style>