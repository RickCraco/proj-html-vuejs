<template>
    <div class="py-4">
        <button class="rounded-pill position-relative border-0" :style="{'background-color':  color}">
            <span>{{ text }}</span>
            <div :style="{'background-color': colorHover}"></div>
        </button>
    </div>
</template>

<script>
export default {
    name: 'Button',
    props: {
        text: String,
        color: String,
        colorHover: String,
    }
}
</script>

<style lang="scss" scoped>
    button{
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
            color: white;
            >div{
                width: 100%;
            }
        }
    }
</style>