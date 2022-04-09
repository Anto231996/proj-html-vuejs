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
                <ul class="d-flex mb-0 gap-5">
                    <li class="d-flex align-items-center text-uppercase fw-bold" v-for="(link, index) in linksNavigation" :key="index">
                        <a :id="(index === activeLink) ? 'active-link' : '' "  @click="changeActiveLink(index)" class="text-decoration-none me-2" :href="link.url">{{ link.title }} </a>
                        <i v-if="link.dropdownArrow !== false" class="fas fa-angle-down text-secondary"></i>
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

            a{
                color: #3C4858;
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