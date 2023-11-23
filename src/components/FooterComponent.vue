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

                </div>
                <div class="col-3 ps-4">

                </div>
            </div>
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
                        color: 'e65334'
                    }
                ]
            }
        }
    }
</script>

<style lang="scss" scoped>
    .my-bg-footer{
        background-color: #273044;
    }

    p{
        font-size: 13px;
    }
</style>