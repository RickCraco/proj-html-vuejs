<template>
    <div class="container">
        <div class="mt-5 justify-content-center row">
            <div class="p-3 col-6">
                <div class="border d-flex align-items-center justify-content-around p-3">
                    <div>
                        <img src="/img/image_box_1-221x231.png" alt="">
                    </div>
                    <div class="ms-3">
                        <h3 class="my-font-size">Become an Instructor</h3>
                        <p class="fs-5">Teach what you love. Masterstudy gives you the tools to create a course.</p>
                        <Button :text="'START TEACHING'" :color="'#FF4450'" :colorHover="'#009B72'"/>
                    </div>
                </div>
            </div>
            <div class="p-3  col-6">
                <div class="border d-flex align-items-center justify-content-around p-3">
                    <div>
                        <img src="/img/image_box_2-234x231.png" alt="">
                    </div>
                    <div class="ms-3">
                        <h3 class="my-font-size">Access For Business</h3>
                        <p class="fs-5">Get unlimited access to 2,500 of top courses for your team.</p>
                        <Button :text="'DOING BUSINESS'" :color="'#FF4450'" :colorHover="'#009B72'"/>
                    </div>
                </div>
            </div>
        </div>
    </div>
</template>

<script>
import Button from './Button.vue';
export default {
    name: 'PartnerComponent',
    components: {
        Button
    }
}
</script>

<style lang="scss" scoped>
.my-font-size {
    font-size: 36px !important;
}
</style>