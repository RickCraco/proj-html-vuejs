<template>
    <div class="d-flex justify-content-center my-bg-img align-items-center">
        <div class="my-margin">
            <h2 class="">
                Limitless learning,<br>more possibilities
            </h2>
            <p>Online courses open the opportunity for learning to almost anyone,<br>regardless of their scheduling commitments.</p>
            <Button :color="'#FF4450'" :text="'READ MORE'"/>
        </div>
    </div>
</template>

<script>
    import Button from './Button.vue';
    export default {
        name: 'ReadMore',
        components: {
            Button
        }
    }
</script>

<style lang="scss" scoped>
    .my-bg-img{
        background-image: url('/img/bg.png');
        width: 100%;
        height: 650px;
        background-repeat: no-repeat;
    }

    .my-margin{
        margin-right: 500px;
        margin-bottom: 200px;
    }

    h2{
        font-size: 50px;
        font-weight: 500;    
    }
    p{
        font-size: 18px;
        font-weight: 600;
    }

</style>