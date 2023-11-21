<template>
    <div class="container mt-4 pt-4">
        <h2>Popular Development Courses</h2>
        <div class="row">
            <CardComponent/>
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

            }
        },
        methods: {

        }
    }
</script>

<style lang="scss" scoped>

</style>