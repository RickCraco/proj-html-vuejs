<template>
    <div class="my-bg-footer pt-5 border-bottom">
        <div class="container">
            <div class="row text-white">
                <div class="col-3">
                    <h5>ABOUT</h5>
                    <p>Created by MasterStudy 2023. Sed nec felis pellentesque, lacinia dui sed, ultricies sapien. Pellentesque orci lectus, consectetur vel, rutrum eu ipsum. Mauris accumsan eros eget libero posuere vulputate.</p>
                </div>
                <div class="col-3 ps-4">
                    <h5>CONTACT</h5>
                    <div>
                        <div>
                            <p>USA, Callifornia 20, First Avenue,<br>Callifornia</p>
                        </div>
                        <div>
                            <p class="m-0">Tel.: +1 212 458 300 32</p>
                            <p>Fax: +1 212 375 24 14</p>
                        </div>
                        <div>
                            <p>info@masterstudy.com</p>
                        </div>
                    </div>
                </div>
                <div class="col-3 ps-4">
                    <h5>SOCIAL NETWORK</h5>
                    <div class="row g-2">
                        <div class="col-3" v-for="icon in socials">
                            <div class="my-col-3" :style="{'background-color': icon.color}">
                                <i :class="icon.icon"></i>
                            </div>
                        </div>
                    </div>
                </div>
                <div class="col-3 ps-4">
                    <img src="/img/Top-udemy-courses-90-percent-off.jpg" alt="">
                </div>
            </div>
        </div>
    </div>
    <div class="my-bg-footer py-4 text-white">
        <div class="container">
            <img src="/img/footer-logo2x-50x56.png" alt="" class="logo-footer">
            <span class="ps-3">Copyright © 2022. MasterStudy Theme by StylemixThemes</span>
        </div>
    </div>
</template>

<script>
    export default {
        name: 'FooterComponent',
        data(){
            return{
                socials: [
                    {
                        icon: 'fa-brands fa-facebook',
                        color: '#4267B2'
                    },
                    {
                        icon: 'fa-brands fa-instagram',
                        color: '#ce40a6'
                    },
                    {
                        icon: 'fa-brands fa-linkedin-in',
                        color: '#006fb9'
                    },
                    {
                        icon: 'fa-brands fa-twitter',
                        color: '#00a3f7'
                    },
                    {
                        icon: 'fa-brands fa-pinterest',
                        color: '#ce1d1a'
                    },
                    {
                        icon: 'fa-solid fa-basketball',
                        color: '#0f99f9'
                    },
                    {
                        icon: 'fa-brands fa-google-plus',
                        color: '#f65f8a'
                    },
                    {
                        icon: 'fa-brands fa-skype',
                        color: '#e65334'
                    }
                ]
            }
        }
    }
</script>

<style lang="scss" scoped>

    .logo-footer{
        width: 30px;
    }

    img{
        width: 250px;
    }

    .my-bg-footer{
        background-color: #273044;
    }

    p{
        font-size: 13px;
    }

    .my-col-3{
        width: 3em;
        height: 3em;
        border-radius: 50%;
        display: flex;
        justify-content: center;
        align-items: center;
        transition: all 0.5s ease;
        font-size: 1em;
        
        i{
            transition: all 0.5s ease;
        }

        &:hover{
            transform: rotateY(180deg);
            i{
                transform: rotateY(180deg);
            }
        }
    }
</style>