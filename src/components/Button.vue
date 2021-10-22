<template>
    <button type="button" @click="handleClick()">
        <Icon v-show="loading" :nameIcon="icon" :rotate="true" />
        <div>{{ title }}</div>
        <Icon :nameIcon="icon" />
    </button>
</template>

<script>
import Icon from '@/components/Icon.vue'

export default {
    name: 'Button',
    components: {
        Icon,
    },
    props: {
        title: String,
        icon: String,
    },
    data() {
        return {
            loading: false,
        }
    },
    methods: {
        handleClick: function () {
            this.loading = !this.loading
        },
    },
}
</script>