<template>
    <div class="container mt-4 pt-4">
        <h2>Popular Development Courses</h2>
        <div class="row py-5">
            <CardComponent v-for="card in popularCourses" :img="card.img" :category="card.category" :text="card.text"
                :voto="card.voto" :price="card.price" :originalPrice="card.originalPrice"/>
        </div>
    </div>
    <ReadMore />
    <div class="container mt-4 pt-4">
        <h2 class="text-center my-fs">Recent Courses</h2>
        <div class="pt-3">
            <ul class="list-unstyled text-center d-flex justify-content-center align-items-center">
                <li class="px-4 rounded-pill py-2" v-for="item in categories">{{ item.name }}</li>
            </ul>
        </div>
        <div class="row py-5">
            <CardComponent v-for="card in recentCourses" :img="card.img" :category="card.category" :text="card.text" :voto="card.voto" :price="card.price" :originalPrice="card.originalPrice"/>
        </div>
        <div class="text-center"><Button :text="'SHOW ALL'" :color="'#457993'"/></div>
    </div>
    <NewsLetter/>
    <div class="container pt-4">
        <h2 class="text-center my-fs">Popular Courses</h2>
        <p class="text-center">Discover our most popular courses for self learning</p>
        <div class="row py-5 g-2 flex-nowrap overflow-hidden scroll-smooth" ref="carosello">
            <CardComponent v-for="card in recentCourses" :img="card.img" :category="card.category" :text="card.text" :voto="card.voto" :price="card.price" :originalPrice="card.originalPrice"/>
        </div>
        <div class="text-center">
            <div class="my-btn" @click="scrollLeft()"><i class="fa-solid fa-chevron-left"></i></div>
            <div class="my-btn" @click="scrollRight()"><i class="fa-solid fa-chevron-right"></i></div>
        </div>
    </div>
    <PartnerComponent/>
    <FutureComponent/>
</template>

<script>
import Button from './Button.vue';
import PartnerComponent from './PartnerComponent.vue';
import NewsLetter from './NewsLetter.vue';
import CardComponent from './CardComponent.vue';
import ReadMore from './ReadMore.vue';
import FutureComponent from './FutureComponent.vue';
export default {
    name: 'MainComponent',
    components: {
        CardComponent,
        ReadMore,
        NewsLetter,
        PartnerComponent,
        FutureComponent,
        Button
    },
    data() {
        return {
            popularCourses: [
                {
                    img: '/img/895786_7b4b_2-272x161.jpg',
                    category: 'Development',
                    text: 'The Complete iOS 10 & Swift 3 Developer Course',
                    voto: 4,
                    originalPrice: '',
                    price: 'Free'
                },
                {
                    img: '/img/246154_d8b0_3-272x161.jpg',
                    category: 'Development',
                    text: 'Web Design for Beginners: Real World Coding in HTML & CSS',
                    voto: 4,
                    originalPrice : '$129.99',
                    price: '$65'
                },
                {
                    img: '/img/752950_b773-272x161.jpg',
                    category: 'Development',
                    text: 'GitHub Ultimate: Master Git and GitHub–Beginner to Expert',
                    voto: 4,
                    originalPrice: '$99.99',
                    price: '$50'
                },
                {
                    img: '/img/1253188_58f7_2-272x161.jpg',
                    category: 'Development',
                    text: 'The Complete iOS 11 & Swift Developer Course–Build 20 Apps',
                    voto: 4,
                    originalPrice: '$199.99',
                    price: '$100'
                },
                {
                    img: '/img/919872_ed54_6-272x161.jpg',
                    category: 'Development',
                    text: 'Android Java Masterclass–Become an App Developer',
                    voto: 4,
                    originalPrice: '$99.99',
                    price: '$50'
                },
                {
                    img: '/img/951684_9c1a_2-272x161.jpg',
                    category: 'Development',
                    text: 'Xamarin Forms: Build Native Cross-platform Apps with C#',
                    voto: 4,
                    originalPrice: '$189.99',
                    price: '$95'
                }
            ],
            categories: [
                {
                    id: '1',
                    name: 'All Categories',
                },
                {
                    id: '2',
                    name: 'Business',
                },
                {
                    id: '3',
                    name: 'Design',
                },
                {
                    id: '4',
                    name: 'Development'
                },
                {
                    id: '5',
                    name: 'IT & SOFTWARE'
                },
                {
                    id: '6',
                    name: 'Lifestyle'
                },
                {
                    id: '7',
                    name: 'Marketing'
                },
                {
                    id: '8',
                    name: 'Office Productivity'
                }
            ],
            recentCourses: [
                {
                    img: '/img/1253188_58f7_2-272x161.jpg',
                    category: 'Development',
                    text: 'The Complete iOS 11 & Swift Developer Course–Build 20 Apps',
                    voto: 4,
                    originalPrice: '',
                    price: 'Free'
                },
                {
                    img: '/img/1561458_7f3b-272x161.jpg',
                    category: 'Design',
                    text: 'CSS – The Complete Guide 2020 (incl. Flexbox, Grid & Sass)',
                    voto: 5,
                    originalPrice: '$199.99',
                    price: '$100'
                },
                {
                    img: '/img/246154_d8b0_3-272x161.jpg',
                    category: 'Development',
                    text: 'Web Design for Beginners: Real World Coding in HTML & CSS',
                    voto: 5,
                    originalPrice: '$129.99',
                    price: '$65'
                },
                {
                    img: '/img/1208228_d61c_4-272x161.jpg',
                    category: 'Design',
                    text: 'Digitally Painting Light and Color: Amateur to Master',
                    voto: 4,
                    originalPrice: '$139.99',
                    price: '$70'
                },
                {
                    img: '/img/186792_41e4_4-272x161.jpg',
                    category: 'Arts & Crafts',
                    text: 'Become an Arabic Calligraphy Artist from Scratch',
                    voto: 5,
                    originalPrice: '',
                    price: '$199.99'
                },
                {
                    img: '/img/1776542_30b1-272x161.jpg',
                    category: 'Google',
                    text: 'Google Searching Ninja',
                    voto: 4,
                    originalPrice: '$89.99',
                    price: '$45'
                },
                {
                    img: '/img/949316_2a64_11-272x161.jpg',
                    category: 'Arts & Crafts',
                    text: 'Foundations for Mastering Watercolor Painting',
                    voto: 5,
                    originalPrice: '$19.99',
                    price: '$10'
                },
                {
                    img: '/img/366802_6fcc-272x161.jpg',
                    category: 'Food & Beverage',
                    text: 'Get Wine-Smart',
                    voto: 4,
                    originalPrice: '$49.99',
                    price: '$25'
                },
                {
                    img: '/img/381588_2e6d_4-272x161.jpg',
                    category: 'Arts & Crafts',
                    text: 'The Colored Pencil Drawing Course',
                    voto: 4,
                    originalPrice: '$34.99',
                    price: '$18'
                },
                {
                    img: '/img/838056_611a_3-272x161.jpg',
                    category: 'Arts & Crafts',
                    text: 'Paint Realistic Watercolor and Botanicals – STUDIO BASICS',
                    voto: 4,
                    originalPrice: '$69.99',
                    price: '$35'
                },
                {
                    img: '/img/1414956_d944_15-272x161.jpg',
                    category: 'Arts & Crafts',
                    text: 'Mastering Brushstrokes – Part 1',
                    voto: 5,
                    originalPrice: '$19.99',
                    price: '$10'
                },
                {
                    img: '/img/1109398_4c13-272x161.jpg',
                    category: 'Arts & Crafts',
                    text: 'Paint Realistic Watercolour and Botanicals – MAGNOLIAS',
                    voto: 5,
                    originalPrice: '$69.99',
                    price: '$35'
                },
            ]
        }
    },
    methods: {
        scrollLeft(){
            this.$refs.carosello.scrollBy(-400, 0);
        },
        scrollRight(){
            this.$refs.carosello.scrollBy(400,0);
        }
    }
}
</script>

<style lang="scss" scoped>
    .my-btn{
        width: 50px;
        height: 50px;
        display: inline-block;
        vertical-align: top;
        line-height: 44px;
        text-align: center;
        color: #e0e0e0;
        border: 1px solid #e0e0e0;
        cursor: pointer;
        transition: 3s ease;
    }

    li{
        &:hover{
            background-color: #457993;
            color: white;
        }
    }

    .my-fs{
        font-size: 50px;
    }

</style>