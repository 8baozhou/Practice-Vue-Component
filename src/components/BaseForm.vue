<template>
    <form
        class="card"
        @submit.prevent="submit"
    >
        <h1 class="text-2xl font-bold mb-6">练习 1</h1>
        <label class="block mb-6">
            <span class="form-label mb-2">手机号码</span>
            <input
                class="form-input"
                placeholder="123-4567-8910"
                type="number"
                v-model="phone"
            />
        </label>
        <div class="mb-8">
            <span class="form-label mb-2">验证码登录</span>
            <div class="flex justify-between items-center">
                <p class="mr-4">暂不设置密码，登录时使用验证码进行登录</p>
                <ToggleInput v-model="codeLoginReceive" />
            </div>
        </div>
        <div class="text-right">
            <button
                type="submit"
                class="btn btn-blue"
            >注册</button>
        </div>
    </form>
</template>

<script>
import ToggleInput from '@/components/ToggleInput.vue'

export default {
    data() {
        return {
            phone: null,
            codeLoginReceive: true
        }
    },
    methods: {
        submit() {
            console.log('submit', {
                phone: this.phone,
                codeLoginReceive: this.codeLoginReceive
            })
        }
    },
    components: {
        ToggleInput,
    },
}
</script>
