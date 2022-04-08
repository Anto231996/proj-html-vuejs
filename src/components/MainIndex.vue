<template>
<main>
    <AboutSection/>
    <KeyFeaturesSection/>
</main>
</template>

<script>
import AboutSection from './AboutSection.vue'
import KeyFeaturesSection from './KeyFeaturesSection.vue'

export default {
    name:'MainIndex',
    components:{
        AboutSection,
        KeyFeaturesSection
    }
}
</script>

<style>

</style>