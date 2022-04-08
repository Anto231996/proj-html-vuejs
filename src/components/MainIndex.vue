<template>
<main>
    <AboutSection/>
    <KeyFeaturesSection/>
    <QuickStartSection/>
    <ToolsSection/>
</main>
</template>

<script>
import AboutSection from './AboutSection.vue'
import KeyFeaturesSection from './KeyFeaturesSection.vue'
import QuickStartSection from './QuickStartSection.vue'
import ToolsSection from './ToolsSection.vue'

export default {
    name:'MainIndex',
    components:{
        AboutSection,
        KeyFeaturesSection,
        QuickStartSection,
        ToolsSection
    }
}
</script>

<style>

</style>