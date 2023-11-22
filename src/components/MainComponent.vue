<template>
    <div class="container mt-4 pt-4">
        <h2>Popular Development Courses</h2>
        <div class="row py-5">
            <CardComponent v-for="card in popularCourses" :img="card.img" :category="card.category" :text="card.text" :voto="card.voto" :price="card.price"/>
        </div>
    </div>
</template>

<script>
    import CardComponent from './CardComponent.vue';
    export default {
        name: 'MainComponent',
        components: {
            CardComponent
        },
        data(){
            return{
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
                ]
            }
        },
        methods: {

        }
    }
</script>

<style lang="scss" scoped>
</style>