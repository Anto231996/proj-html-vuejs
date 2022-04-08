<template>
<!-- HEADER-NAV -->
<header class="my-light-gray-bg fixed-top">
    <nav class="container px-5">
        <div class="row align-items-center">
    <!-- MAIN LOGO -->
            <div class="col">
                <a href="#">
                    <img id="logo-header" src="../assets/img/logo-dark.png" alt="Landrick logo">
                </a>
            </div>
    <!-- /MAIN LOGO -->

    <!-- MENU NAV -->
            <div class="col">
                <ul class="d-flex mb-0 gap-5">
                    <li class="text-uppercase list-unstyled" v-for="(link, index) in linksNavigation" :key="index">
                        <a :id="(index === activeLink) ? 'active-link' : '' "  @click="changeActiveLink(index)" class="text-decoration-none" :href="link.url">{{ link.title }}</a>
                    </li>
                </ul>
            </div>
    <!-- /MENU NAV -->

    <!-- BUTTON NAV -->
            <div class="col">
                <div id="buttons-navigation" class="d-flex justify-content-end align-items-center gap-3">
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
                    url:'#'
                },

                {
                    title: 'landing',
                    url:'#'
                },

                {
                    title: 'pages',
                    url:'#'
                },

                {
                    title: 'docs',
                    url:'#'
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

            div.col a img#logo-header{
                height: 30px;
            }

            a{
                color: #161C2D;
            }
            
            div.col div#buttons-navigation a.square-button{
                height: 40px;
                width: 40px;
                background-color: #2F55D41A;
                display: flex;
                justify-content: center;
                align-items: center;
            }
        }
    }
}
</style>