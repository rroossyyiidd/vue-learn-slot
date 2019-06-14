<template>
    <ChildComponent>
        <h2 slot="title">Title child component</h2>
        <h4 slot="subtitle">Subtitle child component</h4>
    </ChildComponent>
</template>

<script>
import ChildComponent from './components/ChildComponent.vue'
export default {
    name: 'Parent',
    components: {
        ChildComponent
    }
}
</script>

<style>

</style>
