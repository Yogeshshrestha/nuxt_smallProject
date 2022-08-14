<template>
    <div>
        <Nav />
        <div class="container">
            <!-- {{ myRentals }} -->
            <MyItem v-for="rental in myRentals" :key="rental.id" :item="rental" />
        </div>
    </div>
</template>

<script>
import { mapState } from 'vuex';

export default {
    computed: {
        ...mapState(['myRentals'])
    }
}
</script>

<style scoped>
</style>