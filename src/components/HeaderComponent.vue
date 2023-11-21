<template>
    <div class="container d-flex justify-content-between pt-4 border-bottom">
        <div>
            <select name="" id=""></select>
        </div>
        <div>
            <ul class="d-flex list-unstyled align-items-center">
                <li class="px-3">1</li>
                <li class="px-3">2</li>
                <li class="px-3">3</li>
                <li class="px-3">4</li>
                <li class="px-3">5</li>
                <li class="px-3">6</li>
                <li class="px-3">7</li>
                <li class="px-3">8</li>
                <li class="px-3">9</li>
                <li class="px-3">10</li>
                <li class="px-3">11</li>
            </ul>
        </div>
    </div>
    <div class="container d-flex align-items-center mt-3">
        <div>
            <img src="/img/MasterStudy.svg" alt="">
        </div>
        <div class="ps-4">
            <span>CATEGORY</span>
        </div>
        <div class="ps-4">
            <input type="text">
        </div>
        <div>
            <span></span>
            <span></span>
        </div>
        <div class="d-flex align-items-center" id="login">
            <span>scritta</span>
            <button>bottone</button>
            <span>icona</span>
        </div>
    </div>
    <div class="text-center mt-3 text-white py-3 text-align-center" id="div-boack">
        <ul class="list-unstyled text-center d-flex justify-content-center align-items-center">
            <li class="px-5">1</li>
            <li class="px-5">2</li>
            <li class="px-5">3</li>
            <li class="px-5">4</li>
            <li class="px-5">5</li>
        </ul>
    </div>
    <div class="my-bg-red">
        <div class="text-white d-flex align-items-center">
            <div class="ps-5">
                <h1>Udemy Affiliate Sales</h1>
                <h4>Monetize your audience and attract new customers with Udemy!</h4>
            </div>
            <div class="ps-5">
                <img src="/img/slide-1.jpg" alt="">
            </div>
        </div>
    </div>
</template>

<script>
    export default {
        name : 'HeaderComponent',
        data(){
            return{
                pageMenu : [
                    {
                        id : '1',
                        name : 'Home'
                    },
                    {
                        id : '2',
                        name: 'Pages',
                        links: [
                            {
                                id: '1',
                                name: 'shop'
                            },
                            {
                                id : '2',
                                name: 'Features',
                                links : ['About Us']
                            },
                            {
                                id: '3',
                                name : 'Events',
                                links: ['Event Grid', 'Event with Sidebar', 'Single Event']
                            },
                            {
                                id: '4',
                                name: 'Gallery',
                                links : ['Gallery Grid', 'Gallery Masonry', 'Gallery with Sidebar']
                            }
                        ]
                    },
                    {
                        id: '3',
                        name: 'Course Formats',
                        links : ['Default Style', 'Classic Style', 'Udemy Affiliate Style', 'Offline Style', 'Free Courses', 'Course Player']
                    },
                    {
                        id: '4',
                        name: 'Courses'
                    },
                    {
                        id: '5',
                        name: 'Demos',
                        links: []
                    }
                ]
            }
        },
        methods : {

        }
    }
</script>

<style lang="scss" scoped>
    #login{
        margin-left: 500px;
    }
    #div-boack{
        background-color: #273044;
    }
    .my-bg-red{
        background-color: #FF4450;
    }
</style>