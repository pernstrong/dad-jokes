<template>
    <section class="joke-display">
        <p>{{ this.joke.data.joke }} </p>
    </section>
</template>


<script>
export default {
    name: 'Display',
    props: {
        joke: Object,
    }
}
</script>


<style scoped>
    .joke-display {
        height: 35vh;
        text-align: center;
        font-size: 2.5em;
    }
</style>