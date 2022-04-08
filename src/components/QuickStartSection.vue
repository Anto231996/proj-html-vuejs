<template>
<!-- SECTION QUICK START -->
<section class="wrapper mb-5">
    <div class="container py-5">
        <!-- QUICK START TEXT -->
        <div class="row text-center">
            <div class="col-12">
                <h6 class="my-blue-text mb-3">QuickStart</h6>
                <h3 class="mb-4">Awesome isn't it? Let's dive in!</h3>
                <p class="text-secondary mb-5">Start working with <span class="my-blue-text fw-bold">Landrick</span> that can provide everthing you need to generate <br> awareness, drive traffic, connect.</p>
            </div>
        </div>
        <!-- /QUICK START TEXT -->

        <!-- HOW TO INSTALL -->
        <div class="row">
            <div class="col bg-dark p-4 rounded mb-4">
                <ul class="d-flex justify-content-between my-dark-gray rounded border border-secondary mb-3 p-0">
                    <li :class="(index === activeButton) ? 'bg-dark' : '' "  @click="changeActiveButton(index)" class="col btn text-white m-0" v-for="(button, index) in buttonsQuickStart" :key="index">{{ button.name }}</li>
                </ul>
                <div>
                    <span class="text-success me-1">$</span>
                    <span class="text-secondary me-3">{{ buttonsQuickStart[activeButton].localInstall }}</span>
                    <span class="text-success me-1">-g</span>
                    <span class="text-secondary">{{ buttonsQuickStart[activeButton].globalInstall }}</span>
                </div>
            </div>
            <div class="d-flex align-items-center px-0">
                <i class="fas fa-check my-fa-check-green me-2"></i><span class="footer-text text-secondary me-5">Organize your data</span>
                <i class="fas fa-check my-fa-check-green me-2"></i><span class="footer-text text-secondary">Work with any team</span>
            </div>
        </div>
        <!-- /HOW TO INSTALL -->
    </div>
</section>
<!-- /SECTION QUICK START -->
</template>


<script>
export default {
    name:'QuickStartSection',

    data: function(){
        return{
            
            activeButton: 0,

            buttonsQuickStart:[
                {
                    name: 'npm',
                    localInstall:'npm install',
                    globalInstall:'claps.js'
                },

                {
                    name: 'nuget',
                    localInstall:'nuget install',
                    globalInstall:'NuGet.js'
                },

                {
                    name: 'spm',
                    localInstall:'spm install',
                    globalInstall:'SpmPackage.js'
                },

                {
                    name: 'github',
                    localInstall:'github install',
                    globalInstall:'GitHub.js'
                }
            ]
        }
    },

    methods:{
        changeActiveButton(index){
            if (this.buttonsQuickStart[index] !== undefined){
                this.activeButton = index;
            }
        }
    }
}
</script>


<style lang="scss" scoped>

.wrapper{
    width: 700px;
    margin: 0 auto;
}

.my-fa-check-green{
    border: 1px solid #2ECA8B;
    color: #2ECA8B;
}

</style>