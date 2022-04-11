<template>
	<h1>{{ store.foo }}</h1>
</template>

<!-- <script>
export default
{
	async setup()
	{
        const store = createStore({
            state: {
            foo: 'bar'
            }
        })
        return store.state
    }
}
</script> -->

<script setup>
    import { defineExpose } from "vue"
    import { defineStore } from "pinia"

    const store = defineStore('counter', () =>
    {
        return {
            foo: "bar"
        }
    })

    defineExpose({ 
        store
    })
</script>

<style scoped>
h1 
{
  color: red;
}
</style>
