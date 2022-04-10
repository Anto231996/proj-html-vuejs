<template>
<!-- HEADER-NAV -->
<header class="my-light-gray-bg fixed-top">
    <nav class="container px-5">
        <div class="row align-items-center">
    <!-- MAIN LOGO -->
            <div class="col">
                <a href="#">
                    <img class="main-logo" src="../assets/img/logo-dark.png" alt="Landrick logo">
                </a>
            </div>
    <!-- /MAIN LOGO -->

    <!-- MENU NAV -->
            <div class="col">
                <ul class="d-flex p-0 mb-0 gap-4">
                    <li class="list-unstyled text-uppercase fw-bold" v-for="(link, index) in linksNavigation" :key="index">
                        <a :id="(index === activeLink) ? 'active-link-header' : '' "  @click="changeActiveLink(index)" class="d-flex align-items-center text-decoration-none gap-2" :href="link.url">{{ link.title }} <i v-if="link.dropdownArrow !== false" class="fas fa-angle-down"></i></a>
                    </li>
                </ul>
            </div>
    <!-- /MENU NAV -->

    <!-- BUTTON NAV -->
            <div class="col d-none d-lg-inline-block">
                <div id="buttons-navigation" class="d-flex justify-content-end gap-3">
                    <a class="btn">
                        <i class="fas fa-search text-secondary"></i>
                    </a>
                    <a class="square-button btn shadow-sm">
                        <i class="fab fa-github my-blue-text"></i>
                    </a>
                    <a class="square-button btn shadow-sm">
                        <i class="fab fa-stack-overflow my-blue-text"></i>
                    </a>
                    <a class="square-button btn shadow-sm">
                        <i class="fas fa-user my-blue-text"></i>
                    </a>
                </div>
            </div>
    <!-- /BUTTON NAV -->

        </div>
    </nav>
</header>
<!-- /HEADER-NAV -->
</template>


<script>
export default {
    name:'HeaderIndex',

    data:function() {
        return{

            activeLink: 1,

            linksNavigation:[
                {
                    title: 'home',
                    url:'#',
                    dropdownArrow: false
                },

                {
                    title: 'landing',
                    url:'#',
                    dropdownArrow: true
                },

                {
                    title: 'pages',
                    url:'#',
                    dropdownArrow: true
                },

                {
                    title: 'docs',
                    url:'#',
                    dropdownArrow: true
                },
            ]
        }
    },

    methods:{
        changeActiveLink(index){
            if (this.linksNavigation[index] !== undefined){
                this.activeLink = index;
            }
        }
    }
}
</script>


<style lang="scss">

header{
    height: 80px;

    nav.container{
        height: 100%;

        div.row{
            height: 100%;

            ul li a{
                color: #3C4858;
            }

            ul li a:hover{
                color: #2F55D4;
            }
            
            div#buttons-navigation a.square-button{
                height: 40px;
                width: 40px;
                background-color: #2F55D41A;
                display: flex;
                justify-content: center;
                align-items: center;
            }

            div#buttons-navigation a.square-button:hover{
                background-color: #2F55D4;
            }

            div#buttons-navigation a.square-button:hover i{
                color: white;
            }
        }
    }
}
</style>