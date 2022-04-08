<template>
<section>
<!-- SECTION ABOUT -->
    <section id="about" class="border-bottom my-light-gray-bg">
        <div class="container p-5 mb-5">
            <div class="row align-items-center">

    <!-- ABOUT TEXT -->
                <div class="col-6">
                    <pre class="d-inline my-blue-text my-alice-blue-bg border fw-bold">Development</pre>
                    <h1 class="mb-4 fw-bold pt-3">A Complete<br>Developer Toolset</h1>
                    <p class="mb-4 text-secondary">Launch your campaign and benefit from our expertise on designign and managing conversion centered bootstrap4 html page.</p>
                    <div class="mb-4 fw-bold">
                        <a class="me-3 text-decoration-none p-2 text-white my-blue-bg rounded shadow" href="#">Get Started</a>
                        <a class="text-decoration-none p-2 my-blue-text rounded" href="#">Documentation</a>
                    </div>
                    <p class="text-secondary">Current Version: v2.6.0</p>
                </div>
    <!-- /ABOUT TEXT -->
    
    <!-- ABOUT IMG -->
                <div class="col-6 d-flex justify-content-center">
                    <img class="img-fluid" src="../assets/img/about.png" alt="ragazzo seduto al pc">
                </div>
    <!-- /ABOUT IMG -->

            </div>
        </div>
    </section>
<!-- /SECTION ABOUT -->

<!-- SECTION SPONSOR-BRANDS -->
    <section id="sponsor-brands" class="my-light-gray-bg p-5 mb-5">
        <div class="container">
            <div class="row">
                <img class="col-2" v-for="(sponsor, index) in sponsorBrands" :key="index" :src="require(`../assets/img/${sponsor.logo}`)" :alt="sponsor.name + ' ' + 'logo'">
            </div>
        </div>
    </section>
<!-- /SECTION SPONSOR-BRANDS -->
</section>
</template>


<script>
export default {
    name: 'AboutSection',

    data: function () {
        return{
            sponsorBrands:[
                {
                    name:'Amazon',
                    logo:'amazon.svg',
                },

                {
                    name:'Google',
                    logo:'google.svg',
                },

                {
                    name:'Lenovo',
                    logo:'lenovo.svg',
                },

                {
                    name:'PayPal',
                    logo:'paypal.svg',
                },

                {
                    name:'Shopify',
                    logo:'shopify.svg',
                },

                {
                    name:'Spotify',
                    logo:'spotify.svg',
                },
            ]
        }
    }
}
</script>


<style lang="scss">
section#about{
    padding-top: 150px;

    pre{
        font-size: .8rem;
        padding: .3rem;
        border-radius: 15px;
    }

    a{
        border: 1px solid #2F55D4;
    }
}

section#sponsor-brands{
    img{
        height: 30px;
    }
}
</style>