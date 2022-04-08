<template>
<!-- SECTION KEY FEATURES -->
<section class="container p-5 mb-5">
    <!-- FEATURES TEXT -->
    <div class="row mb-5">
        <div class="col-5">
            <h3 class="fw-bold">Key Features</h3>
            <p class="text-secondary">Start Working with <span class="my-blue-text fw-bold">Landrick</span> that can provide everything you need to generate awareness, drive traffic, connect</p>
        </div>
    </div>
    <!-- /FEATURES TEXT -->

    <!-- FEATURES CARDS -->
    <div class="row">
        <div class="feature-card col-3 p-2" v-for="(card, index) in featureCards" :key="index">
            <div class="border rounded p-4">
                <div class="square-bg d-flex justify-content-center align-items-center rounded mb-4">
                    <i :class="card.icon" class="fa-2x my-blue-text"></i>
                </div>
                <h6 class="fw-bold">{{ card.title }}</h6>
                <p class="text-secondary">Composed in a pseudo-Latin language which more or less corresponds.</p>
                <a class="my-blue-text text-decoration-none fw-bold" href="#">Read More <i class="fas fa-angle-right"></i></a>
            </div>
        </div>
    </div>
    <!-- /FEATURES CARDS -->
</section>
<!-- /SECTION KEY FEATURES -->
</template>


<script>

export default {
    name: 'KeyFeaturesSection',

    data: function(){
        return{
            featureCards:[
                {
                    icon: 'far fa-copy',
                    title: 'Modular'
                },

                {
                    icon: 'fas fa-tv',
                    title: 'Responsive'
                },

                {
                    icon: 'far fa-image',
                    title: 'Customizable'
                },

                {
                    icon: 'fas fa-expand-arrows-alt',
                    title: 'Scalable'
                }
            ]
        }
    }
}

</script>


<style lang="scss">

div.feature-card:hover{
    position: relative;
    bottom: 10px;
}

.square-bg{
    height: 60px;
    width: 60px;
    background-color: #2F55D41A;
}

</style>