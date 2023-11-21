<template>
    <div class="container mt-4 pt-4">
        <h2>Popular Development Courses</h2>
        <div class="row">
            <CardComponent v-for="n in 5"/>
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
                        img: '',
                        category: '',
                        text: '',
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