<template>
<p>Reaction time is : {{ score }} milliseconds</p>
<p class="rank">{{ rank }}</p>
</template>

<script>
export default {
    props: ['score'],
    data() {
        return {
            rank: null
        }
    },
    mounted() {
        if (this.score < 300) {
            this.rank = 'Rapid Reflex'
        } else if (this.score < 400) {
            this.rank = 'Fast Reflex'
        } else {
            this.rank = 'Slow Reflex'
        }
    }
}
</script>

<style>
.rank {
    font-size: 1.4em;
    color: #0faf87;
    font-weight: bold;
}
</style>