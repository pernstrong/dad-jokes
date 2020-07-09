<template>
    <section class="button-section">
       <button @click="$emit('get-joke')">New Joke</button>
    </section>
</template>


<script>
export default {
    name: 'Button',
    props: ['getJoke']
}
</script>

<style scoped>
    button {
        font-size: 1.4em;
        padding: 5% 2%;
        border-radius: 10px;
        width: 80%;
        margin: 0% 10%;
    }
</style>