<template>
    <h4>{{ score }} ms</h4>
    <h3 class="rank">{{ rank }}</h3>
</template>

<script>
export default {
    props: ["score"],
    data() {
        return{
            rank: null
        }
    },
    mounted() {
        if(this.score <= 250) {
            this.rank = 'SuperFast'
        } else if (this.score <= 400) {
            this.rank = 'Fast'
        } else {
            this.rank = 'slow'
        }
    }
}
</script>

<style>
    .rank {
        color: #0fad87;
    }
</style>