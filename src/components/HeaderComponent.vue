<template>
    <div class="container d-flex justify-content-between pt-4 border-bottom">
        <div>
            <select name="" id="">
                <option value="">ENGLISH</option>
            </select>
        </div>
        <div class="d-flex align-items-center">
            <ul class="d-flex list-unstyled align-items-center">
                <li class="px-3" v-for="item in pageMenu">{{ item.name }}</li>
            </ul>
            <ul class="d-flex list-unstyled align-items-center">
                <li class="px-3"><i class="fa-brands fa-facebook"></i></li>
                <li class="px-3"><i class="fa-brands fa-twitter"></i></li>
                <li class="px-3"><i class="fa-brands fa-instagram"></i></li>
                <li class="px-3"><i class="fa-brands fa-linkedin"></i></li>
                <li class="px-3"><i class="fa-brands fa-google-plus"></i></li>
                <li class="px-3"><i class="fa-brands fa-youtube"></i></li>
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
            <li class="px-5" v-for="item in courseMenu">{{ item.name }}</li>
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
                ],
                courseMenu: [
                    {
                        id : '1',
                        name : 'Business',
                        links : []
                    },
                    {
                        id : '2',
                        name : 'Design',
                        links : []
                    },
                    {
                        id: '3',
                        name: 'Development',
                        links: []
                    },
                    {
                        id: '4',
                        name: 'Lifestyle',
                        links: []
                    },
                    {
                        id: '5',
                        name: 'Office Productivity',
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