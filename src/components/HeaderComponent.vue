<template>
    <div class="overflow-hidden">
        <div class="border-bottom">
            <div class="container d-flex justify-content-between pt-4">
                <div>
                    <select name="" id="" class="border-0">
                        <option value="">ENGLISH</option>
                    </select>
                </div>
                <div class="d-flex align-items-center">
                    <ul class="d-flex list-unstyled align-items-center">
                        <li class="px-3 position-relative itemmenu" v-for="item in pageMenu">
                            {{ item.name }}
                            <ul class="submenu p-0 ps-2" v-if="item.links.length">
                                <li v-for="subitem in item.links">
                                    {{ subitem.name }}
                                    <ul class="sub-sub-menu" v-if="subitem.links.length">
                                        <li v-for="subsubitem in subitem.links">{{ subsubitem }}</li>
                                    </ul>
                                </li>
                            </ul>
                        </li>
                    </ul>
                    <ul class="d-flex list-unstyled align-items-center">
                        <li class="px-3"><i class="fa-brands fa-facebook"></i></li>
                        <li class="px-3"><i class="fa-brands fa-twitter"></i></li>
                        <li class="px-3"><i class="fa-brands fa-instagram"></i></li>
                        <li class="px-3"><i class="fa-brands fa-linkedin"></i></li>
                        <li class="px-3"><i class="fa-brands fa-google-plus"></i></li>
                        <li class="px-3"><i class="fa-brands fa-youtube"></i></li>
                    </ul>
                </div>
            </div>
        </div>
        <div class="container d-flex align-items-center mt-3">
            <div>
                <img src="/img/MasterStudy.svg" alt="">
            </div>
            <div class="ps-4">
                <span class="itemmenu">
                    <i class="fa-solid fa-bars"></i> CATEGORY
                    <ul class="submenu">
                        <li v-for="item in courseMenu" class="py-2">
                            {{ item.name }}
                            <ul class="sub-sub-menu d-flex flex-column flex-wrap">
                                <li v-for="subitem in item.links" class="py-2">{{ subitem }}</li>
                            </ul>
                        </li>
                    </ul>
                </span>
            </div>
            <div class="ps-4">
                <input type="text" class="">
            </div>
            <div>
                <span></span>
                <span></span>
            </div>
            <div class="d-flex align-items-center" id="login">
                <span>scritta</span>
                <button>bottone</button>
                <span>icona</span>
            </div>
        </div>
        <div class="text-center mt-3 text-white text-align-center" id="div-boack">
            <ul class="list-unstyled text-center d-flex justify-content-center align-items-center position-relative big-menu h-100 m-0">
                <li class="px-5 py-4 my-bg-hover" v-for="item in courseMenu"><i :class="item.icon"></i>
                    {{ item.name }}
                    <ul class="row list-unstyled big-sub-menu">
                        <li v-for="subitem in item.links" class="col-3">{{ subitem }}</li>
                    </ul>
                </li>
            </ul>
        </div>
        <div class="my-bg-red mt-5">
            <div class="text-white d-flex align-items-center">
                <div class="ps-3">
                    <h1 class="">Udemy Affiliate Sales</h1>
                    <h4 class="">Monetize your audience and attract new customers with Udemy!</h4>
                </div>
                <div class="my-slide">
                    <img src="/img/slide-1.jpg" alt="">
                </div>
            </div>
        </div>
    </div>
</template>

<script>
export default {
    name: 'HeaderComponent',
    data() {
        return {
            pageMenu: [
                {
                    id: '1',
                    name: 'Home',
                    links: []
                },
                {
                    id: '2',
                    name: 'Pages',
                    links: [
                        {
                            id: '1',
                            name: 'shop',
                            links: []
                        },
                        {
                            id: '2',
                            name: 'Features',
                            links: ['About Us']
                        },
                        {
                            id: '3',
                            name: 'Events',
                            links: ['Event Grid', 'Event with Sidebar', 'Single Event']
                        },
                        {
                            id: '4',
                            name: 'Gallery',
                            links: ['Gallery Grid', 'Gallery Masonry', 'Gallery with Sidebar']
                        }
                    ]
                },
                {
                    id: '3',
                    name: 'Course Formats',
                    links: [
                        {
                            name: 'Default Style',
                            links: []
                        },
                        {
                            name: 'Classic Style',
                            links: []
                        },
                        {
                            name: 'Udemy Affiliate Style',
                            links: []
                        },
                        {
                            name: 'Offline Style',
                            links: []
                        },
                        {
                            name: 'Free Courses',
                            links: ['Default Style', 'Classic Style', 'Udemy Style', 'Offline Style']
                        }
                    ]
                },
                {
                    id: '4',
                    name: 'Courses',
                    links: []
                },
                {
                    id: '5',
                    name: 'Demos',
                    links: [
                        {
                            name: 'Udemy Affiliate',
                            links: []
                        },
                        {
                            name: 'Light LMS',
                            links: []
                        },
                        {
                            name: 'Dark LMS',
                            links: []
                        },
                        {
                            name: 'Architecture',
                            links: []
                        },
                        {
                            name: 'Coding School',
                            links: []
                        },
                        {
                            name: 'Online Academy',
                            links: []
                        },
                        {
                            name: 'Offline Courses',
                            links: []
                        }
                    ]
                }
            ],
            courseMenu: [
                {
                    id: '1',
                    name: 'Business',
                    icon: 'fa-solid fa-chart-column',
                    links: ['Communications', 'Entrepreneurship', 'Home Business', 'Media', 'Data & Analytics', 'Finance', 'Human Resources', 'Sales']
                },
                {
                    id: '2',
                    name: 'Design',
                    icon: 'fa-solid fa-palette',
                    links: ['3D Animation', 'Desing Thinking', 'Game Design', 'Other', 'Web Design', 'Architectural Design', 'Design Tools', 'Graphic Design', 'User Experience']
                },
                {
                    id: '3',
                    name: 'Development',
                    icon: 'fa-solid fa-gear',
                    links: ['Data Science', 'Development Tools', 'Game Development', 'Programming Languages', 'Software Testing', 'Databases', 'E-commerce', 'Mobile Apps', 'Software Engineering', 'Web Development']
                },
                {
                    id: '4',
                    name: 'Lifestyle',
                    icon: 'fa-regular fa-face-smile',
                    links: ['Arts & Crafts', 'Foode & Beverage', 'Home Improvement', 'Travel', 'Beauty & Makeup', 'Gaming', 'Pet Care & Training']
                },
                {
                    id: '5',
                    name: 'Office Productivity',
                    icon: 'fa-solid fa-print',
                    links: ['Apple', 'Google', 'SAP', 'Microsoft', 'Oracle']
                }
            ]
        }
    },
    methods: {

    }
}
</script>

<style lang="scss" scoped>
.my-slide {
    padding-left: 500px;
}

#login {
    margin-left: 500px;
}

#div-boack {
    background-color: #273044;
}

.my-bg-red {
    background-color: #FF4450;
}

.my-bg-hover{
    transition: all 0.4s ease;
    height: 100%;
    &:hover{
        background-color: #457993;
       
    }
}

.itemmenu {

    position: relative;

    &:hover {
        .submenu {
            z-index: 1;
            opacity: 1;
            top: 100%;
        }
    }

    .submenu {
        position: absolute;
        top: 120%;
        left: 0;
        z-index: -1;
        opacity: 0;
        transition: all 0.3s ease;
        background-color: white;
        list-style: none !important;
        border-top: 2px solid red;
        width: 300px;

        >li:hover {
            .sub-sub-menu {
                z-index: 1;
                opacity: 1;
                left: 100%;
            }
        }

        .sub-sub-menu {
            position: absolute;
            top: 0;
            left: 120%;
            z-index: -1;
            opacity: 0;
            transition: all 0.3s ease;
            background-color: grey;
            list-style: none;
            width: 450px;
            height: 100%;
        }
    }

}

.big-menu {

    > li:hover{
        .big-sub-menu{
            opacity: 1;
            z-index: 1;
        }
    }
    .big-sub-menu {
        position: absolute;
        top: 100%;
        left: 50%;
        z-index: -1;
        opacity: 0;
        transition: all 0.3s ease;
        background-color: #457993;
        width: 1300px !important;
        transform: translateX(-50%);
    }
}
</style>