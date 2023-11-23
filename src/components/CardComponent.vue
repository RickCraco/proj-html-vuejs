<template>
    <div class="col-3 p-2">
        <div class="border p-3 h-100">
            <img :src="img" class="card-img" alt="">
            <div class="card-body">
                <h5 class="card-title my-1">{{ category }}</h5>
                <p class="card-text border-bottom pb-2">{{ text }}</p>
                <div class="d-flex justify-content-between">
                    <p>{{ voto }}</p>
                    <span>
                        <p class="m-0 text-decoration-line-through">{{ originalPrice }}</p> 
                        {{ price }}
                    </span>
                </div>
            </div>
        </div>
    </div>
</template>

<script>
export default {
    name: 'CardComponent',
    props: {
        img: String,
        category: String,
        text: String,
        voto: Number,
        price: String,
        originalPrice: String,
    },
    data() {
        return {

        }
    },
    methods: {

    }
}
</script>

<style lang="scss" scoped>
    span{
        display: block;
    }
</style>