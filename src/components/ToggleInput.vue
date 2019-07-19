<template>
    <span
        class="toggle"
        role="checkbox"
        tabindex="0"
        :aria-checked="toggled.toString()"
        @click="$emit('toggle', !toggled)"
        @keydown.space.prevent="$emit('toggle', !toggled)"
    ></span>
</template>

<script>
export default {
    model: {
        prop: 'toggled',
        event: 'toggle'
    },
    props: ['toggled'],
}
</script>

<style>
</style>