<template>
    <div class="mt-4 py-4">
        <button class="btn position-relative">
            <span>READ MORE</span>
            <div></div>
        </button>
    </div>
</template>

<script>
export default {
    name: 'Button'
}
</script>

<style lang="scss" scoped>
    button{
        background-color: #FF4450;
        color: white;
        padding: 20px;
        padding-left: 40px;
        padding-right: 40px;
        border-radius: 35px;
        overflow: hidden;

        >span{
            z-index: 200;
            position: relative;
        }

        >div{
            height: 100%;
            width: 0px;
            transition: all 0.5s ease;
            position: absolute;
            left: 0;
            top: 0;
            z-index: 1;
            background-color: rgba($color: #000000, $alpha: 0.2);
        }

        &:hover{
            background-color: #FF4450;
            color: white;
            >div{
                width: 100%;
            }
        }
    }
</style>