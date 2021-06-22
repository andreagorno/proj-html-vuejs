<template>
    <footer>
        <img src="../assets/img/logo-img-01.png" alt="logo">
        <p>
            Sometimes doing something seemingly demanding turns out to be fun. <br>
            Here's the proof - Bryson, your brand new portfolio.
        </p>
        <div class="media">
            <div 
            v-for="(item, index) in items"
            :key="index"
            >
                
                <a :href="item.url">
                    <i :class="`fab ${item.code} ${item.bgcolor}`"></i>
                </a>
                
            </div>
        </div>
    </footer>
</template>

<script>
export default {
    name: "Footer",

    props: {
        items: [ Array ],
    }
}
</script>

<style lang="scss" scoped>
    @import "../style/variables.scss";

    footer {
        display: flex;
        flex-direction: column;
        justify-content: center;
        align-items: center;
        height: 300px;
        text-align: center;
        background-image: url("../assets/img/h2-footer-img-01.jpg");
        background-size: cover;

        img {
            height: 25px;
        }

        p {
            font-size: 12px;
            color: $mainTextColor2;
            margin: 20px;
        }

        .media {
            display: flex;

            i { 
                display: inline-block;
                width: 30px;
                height: 30px;
                margin: 0 10px;
                color: white;
                padding: 7px 5px 5px 5px;
                border-radius: 50%;
                cursor: pointer;
            }

        }
        .blue {
            background-color: #69A9AA;
        }
        .yellow {
            background-color: #EEC681;
        }
        .pink {
            background-color: #F7BCA8;
        }
        .lightgreen {
            background-color: #C2BF7D;
        }

    }
</style>