<template>
    <div>
        <Nav />
        <div class="container">
            <LargeCardDisplay v-for="cardInfo in largeCardInfo.slice(0, 1)" :key="cardInfo.id"
                :cardsSection="cardInfo" />
            <SmallCardDisplay v-for="cardInfo in smallCardsSections" :key="cardInfo.id" :cardsSection="cardInfo" />
        </div>
    </div>
</template>

<script>
import { largeCardSections, smallCardSections } from '../../assets/data.js';
import LargeCardDisplay from '../../../clone/Nuxt-Crash-Course/Client/components/LargeCardDisplay.vue';
export default {
    components: { LargeCardDisplay },

    data() {
        return {
            largeCardInfo: largeCardSections,
            smallCardsSections: smallCardSections
        }
    }
}
</script>

<style scoped>
</style>