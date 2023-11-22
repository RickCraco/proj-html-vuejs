<template>
    <div class="d-flex justify-content-center my-bg-img align-items-center">
        <div class="my-margin">
            <h2 class="">
                Limitless learning,<br>more possibilities
            </h2>
            <p>Online courses open the opportunity for learning to almost anyone,<br>regardless of their scheduling commitments.</p>
            <div class="mt-4 py-4">
                <button class="btn position-relative">
                    <span>READ MORE</span>
                    <div></div>
                </button>
            </div>
        </div>
    </div>
</template>

<script>
    export default {
        name: 'ReadMore',
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