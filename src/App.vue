<template>
    <div
        id="app"
        class="min-h-screen bg-gray-700 p-8"
    >
        <div class="max-w-md mx-auto">
            <BaseForm />
        </div>
    </div>
</template>

<script>
import BaseForm from '@/components/BaseForm.vue'
export default {
    name: 'app',
    components: {
        BaseForm,
    }
}
</script>

<style src="@/assets/css/main.css">
</style>
