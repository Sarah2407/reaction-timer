<template>
    <div class="results">
        <p> Reaction time: {{ results }}ms </p>
        <p class="rank">{{ rank }}</p>
    </div>
  
</template>

<script>
export default {
    props: ['results'],
    data() {
        return {
            rank: null
        }
    },
    mounted() {
        if (this.results < 350) {
            this.rank = 'Awesome fingers'
        }
        else if (this.results < 500) {
            this.rank = 'Good reflexes'
        }
        else {
            this.rank = 'Snail pace'
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