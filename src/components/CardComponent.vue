<template>
    <div class="col-4 m-3 border" style="width: 18rem;">
        <img :src="img" class="card-img" alt="">
        <div class="card-body">
            <h5 class="card-title my-1">{{ category }}</h5>
            <p class="card-text">{{ text }}</p>
            <p>{{ voto }}</p>
            <span>{{ price }}</span>
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
    },
    data() {
        return {

        }
    },
    methods: {

    }
}
</script>

<style lang="scss" scoped></style>