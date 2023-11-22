<template>
    <div class="container mt-4 pt-4">
        <h2>Popular Development Courses</h2>
        <div class="row py-5">
            <CardComponent v-for="card in popularCourses" :img="card.img" :category="card.category" :text="card.text"
                :voto="card.voto" :price="card.price" />
        </div>
    </div>
    <ReadMore />
    <div class="container mt-4 pt-4">
        <h2 class="text-center">Recent Courses</h2>
        <div class="pt-3">
            <ul class="list-unstyled text-center d-flex justify-content-center align-items-center">
                <li class="px-4" v-for="item in categories">{{ item.name }}</li>
            </ul>
        </div>
        <div class="row py-5">
            <CardComponent v-for="card in recentCourses" :img="card.img" :category="card.category" :text="card.text" :voto="card.voto" :price="card.price"/>
        </div>
        <div class="text-center"><button>Show All</button></div>
    </div>
    <NewsLetter/>
    <div class="container pt-4">
        <h2 class="text-center">Popular Courses</h2>
        <p class="text-center">Discover our most popular courses for self learning</p>
        <div class="row py-5">
            <CardComponent v-for="card in recentCourses" :img="card.img" :category="card.category" :text="card.text" :voto="card.voto" :price="card.price"/>
        </div>
    </div>
</template>

<script>
import NewsLetter from './NewsLetter.vue';
import CardComponent from './CardComponent.vue';
import ReadMore from './ReadMore.vue';
export default {
    name: 'MainComponent',
    components: {
        CardComponent,
        ReadMore,
        NewsLetter
    },
    data() {
        return {
            popularCourses: [
                {
                    img: '/img/895786_7b4b_2-272x161.jpg',
                    category: 'Development',
                    text: 'The Complete iOS 10 & Swift 3 Developer Course',
                    voto: 4,
                    price: 'Free'
                },
                {
                    img: '/img/246154_d8b0_3-272x161.jpg',
                    category: 'Development',
                    text: 'Web Design for Beginners: Real World Coding in HTML & CSS',
                    voto: 4,
                    price: 'Free'
                },
                {
                    img: '/img/752950_b773-272x161.jpg',
                    category: 'Development',
                    text: 'GitHub Ultimate: Master Git and GitHub–Beginner to Expert',
                    voto: 4,
                    price: 'Free'
                },
                {
                    img: '/img/1253188_58f7_2-272x161.jpg',
                    category: 'Development',
                    text: 'The Complete iOS 11 & Swift Developer Course–Build 20 Apps',
                    voto: 4,
                    price: 'Free'
                },
                {
                    img: '/img/919872_ed54_6-272x161.jpg',
                    category: 'Development',
                    text: 'Android Java Masterclass–Become an App Developer',
                    voto: 4,
                    price: 'Free'
                },
                {
                    img: '/img/951684_9c1a_2-272x161.jpg',
                    category: 'Development',
                    text: 'Xamarin Forms: Build Native Cross-platform Apps with C#',
                    voto: 4,
                    price: 'Free'
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
                    price: 'Free'
                },
                {
                    img: '/img/246154_d8b0_3-272x161.jpg',
                    category: 'Design',
                    text: 'CSS – The Complete Guide 2020 (incl. Flexbox, Grid & Sass)',
                    voto: 5,
                    price: 'Free'
                },
                {
                    img: '/img/246154_d8b0_3-272x161.jpg',
                    category: 'Development',
                    text: 'Web Design for Beginners: Real World Coding in HTML & CSS',
                    voto: 4,
                    price: 'Free'
                },
                {
                    img: '/img/246154_d8b0_3-272x161.jpg',
                    category: 'Development',
                    text: 'Web Design for Beginners: Real World Coding in HTML & CSS',
                    voto: 4,
                    price: 'Free'
                },
                {
                    img: '/img/246154_d8b0_3-272x161.jpg',
                    category: 'Development',
                    text: 'Web Design for Beginners: Real World Coding in HTML & CSS',
                    voto: 4,
                    price: 'Free'
                },
                {
                    img: '/img/246154_d8b0_3-272x161.jpg',
                    category: 'Development',
                    text: 'Web Design for Beginners: Real World Coding in HTML & CSS',
                    voto: 4,
                    price: 'Free'
                },
                {
                    img: '/img/246154_d8b0_3-272x161.jpg',
                    category: 'Development',
                    text: 'Web Design for Beginners: Real World Coding in HTML & CSS',
                    voto: 4,
                    price: 'Free'
                },
                {
                    img: '/img/246154_d8b0_3-272x161.jpg',
                    category: 'Development',
                    text: 'Web Design for Beginners: Real World Coding in HTML & CSS',
                    voto: 4,
                    price: 'Free'
                },
                {
                    img: '/img/246154_d8b0_3-272x161.jpg',
                    category: 'Development',
                    text: 'Web Design for Beginners: Real World Coding in HTML & CSS',
                    voto: 4,
                    price: 'Free'
                },
                {
                    img: '/img/246154_d8b0_3-272x161.jpg',
                    category: 'Development',
                    text: 'Web Design for Beginners: Real World Coding in HTML & CSS',
                    voto: 4,
                    price: 'Free'
                },
                {
                    img: '/img/246154_d8b0_3-272x161.jpg',
                    category: 'Development',
                    text: 'Web Design for Beginners: Real World Coding in HTML & CSS',
                    voto: 4,
                    price: 'Free'
                },
                {
                    img: '/img/246154_d8b0_3-272x161.jpg',
                    category: 'Development',
                    text: 'Web Design for Beginners: Real World Coding in HTML & CSS',
                    voto: 4,
                    price: 'Free'
                },
            ]
        }
    },
    methods: {

    }
}
</script>

<style lang="scss" scoped></style>