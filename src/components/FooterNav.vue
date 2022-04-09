<template>
<!-- FOOTER NAV -->
<section>
    <div class="container p-5">
        <div class="row">
            <!-- SOCIAL -->
            <div class="col-3">
                <a href="#">
                    <img class="main-logo mb-4" src="../assets/img/logo-light.png" alt="Landrick logo">
                </a>
                <p class="text-secondary mb-4">Start working with Landrick that can provide everthing you need to generate awareness, drive traffic, connect.</p>
                <div class="text-white fa-2x">
                    <i class="fab fa-facebook-square me-2"></i>
                    <i class="fab fa-instagram-square me-2"></i>
                    <i class="fab fa-twitter-square me-2"></i>
                    <i class="fab fa-linkedin"></i>
                </div>
            </div>
            <!-- /SOCIAL -->

            <!-- LINKS -->
            <div class="col-3 d-flex flex-column align-items-center">
                <h5 class="text-white mb-4">Company</h5>
                <ul class="p-0">
                    <li class="list-unstyled mb-2" v-for="(link, index) in companyListLinks" :key="index">
                        <i class="fas fa-angle-right text-secondary me-2"></i><a class="text-decoration-none text-secondary" :href="link.URL">{{ link.name }}</a>
                    </li>
                </ul>
            </div>
            <div class="col-3">
                <h5 class="text-white mb-4">Usefull Links</h5>
                <ul class="p-0">
                    <li class="list-unstyled mb-2" v-for="(link, index) in usefullLinks" :key="index">
                        <i class="fas fa-angle-right text-secondary me-2"></i><a class="text-decoration-none text-secondary" :href="link.URL">{{ link.name }}</a>
                    </li>
                </ul>
            </div>
            <!-- /LINKS -->

            <!-- NEWSLETTER -->
            <div class="col-3">
                <h5 class="text-white mb-4">Newsletter</h5>
                <p class="text-secondary">Sign up and receive the latest tips via email.</p>
                <p class="text-secondary fw-bold">Write your email <span class="text-danger">*</span></p>
                <form class="row g-3">
                    <input type="email" id="inputEmail" class="form-control text-white" placeholder="Your email:">
                    <button type="submit" id="btn-subscribe" class="btn text-primary">Subscribe</button>
                </form>
            </div>
            <!-- /NEWSLETTER -->
        </div>
    </div>
</section>
<!-- /FOOTER NAV -->
</template>


<script>
export default {
    name: 'FooterNav',

    data: function () {
        return{
            companyListLinks:[
                {
                    name:'About us',
                    URL:'#'
                },

                {
                    name:'Services',
                    URL:'#'
                },

                {
                    name:'Team',
                    URL:'#'
                },

                {
                    name:'Pricing',
                    URL:'#'
                },

                {
                    name:'Project',
                    URL:'#'
                },

                {
                    name:'Careers',
                    URL:'#'
                },

                {
                    name:'Blog',
                    URL:'#'
                },

                {
                    name:'Login',
                    URL:'#'
                }
            ],

            usefullLinks:[
                {
                    name:'Terms of Services',
                    URL:'#'
                },

                {
                    name:'Privacy Policy',
                    URL:'#'
                },

                {
                    name:'Documentation',
                    URL:'#'
                },

                {
                    name:'Changelog',
                    URL:'#'
                },

                {
                    name:'Components',
                    URL:'#'
                }
            ]
        }
    }
}
</script>


<style lang="scss" scoped>

    section{
        border-bottom: 1px solid rgba(255, 255, 255, .1);

        input#inputEmail{
            background-color: #27314F;
            border: #27314F;
        }

        button#btn-subscribe{
            background-color: #222E51;
        }
    }

</style>