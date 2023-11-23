<template>
    <div class="mt-5 my-bg-img" v-if="!flag">
        <div class="bg-white my-square-div">
            <h2>Investing for Your Future</h2>
            <p>It is no exaggeration to say this MasterStudy experience was transformative–both professionally and personally. This workshop will long remain a high point of my life. Thanks again…. I am feeling energized and eager to start teaching my class next week. I can’t wait to use all of my new teaching tools. I will absolutely recommend this workshop to other educators!</p>
            <h5>Linda Green</h5>
            <span>Product Manager, Apple Inc</span>
        </div>
    </div>
    <div class="mt-5 my-bg-img-second" v-else>
        <div class="bg-white my-square-div">
            <h2>Paints of the Future</h2>
            <p>The response to your MasterStudy has been really overwhelming! Those who participated in the workshop are spreading the word here on campus and the “buzz” is on. The VP of Instruction wants you to come back! Her goal is to have more faculty trained. She also wants to attend a workshop herself. Our President told me Masterstudy needs to be the cornerstone of our success program.”</p>
            <h5>Xatashi Froust</h5>
            <span>SEO, Froust Inc</span>
        </div>
    </div>
</template>

<script>
    export default {
        name: 'FutureComponent',
        data(){
            return{
                flag: false
            }
        },
        methods: {
            changeDiv(){
                setInterval(() =>{
                    this.flag = true;
                }, 7000)
                setInterval(() =>{
                    this.flag = false;
                }, 14000)
            }
        },
        mounted(){
            this.changeDiv();
        }
    }
</script>

<style lang="scss" scoped>
    .my-square-div{
        width: 600px;
        height: 400px;
        background-color: white;
        color: black;
        padding-left: 30px;
        padding-right: 30px;
        padding-top: 30px;
        margin-left: 400px;
    }
    .my-bg-img{
        background-image: url('/img/testimonial-1-1917x640-1-1914x639.jpg');
        background-repeat: no-repeat;
        padding-top: 120px;
        padding-bottom: 120px;
        background-size: cover;
    }
    .my-bg-img-second{
        background-image: url('/img/micah-296507-unsplash-1-copy-1-1920x700-1-1917x699.jpg');
        background-repeat: no-repeat;
        padding-top: 120px;
        padding-bottom: 120px;
        background-size: cover;
    }
</style>