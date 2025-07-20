<template>
    <button
        @click="handleClick"
        :class="`p-5 m-2 rounded-full backdrop-blur-lg border border-white/10 bg-black shadow-lg hover:shadow-2xl hover:scale-110 hover:rotate-3 active:scale-95 active:rotate-0 transition-all duration-300 ease-out cursor-pointer group relative overflow-hidden ${hoverBorderClass}`">
        <div
            class="absolute inset-0 bg-gradient-to-r from-transparent via-white/10 to-transparent -translate-x-full group-hover:translate-x-full transition-transform duration-700 ease-out">
        </div>
        <div class="relative z-10">
            <img v-if="icon === 'linkedin'" src="/img/linkedin.svg" alt="Instagram" class="w-7 h-7" />
            <img v-else-if="icon === 'instagram'" src="/img/instagram.svg" alt="Instagram" class="w-7 h-7" />
            <img v-else-if="icon === 'outlook'" src="/img/outlook.svg" alt="Instagram" class="w-7 h-7" />
        </div>
    </button>
</template>

<script>
export default {
    name: 'ContactButton',
    props: {
        icon: {
            type: String,
            required: true
        },
        color: {
            type: String,
            required: true
        },
        refUrl : {
            type: String,
            required: false
        }
    },
    computed: {
        hoverBorderClass() {
            if (this.icon === 'linkedin') return 'hover:border-blue-400';
            if (this.icon === 'instagram') return 'hover:border-pink-400';
            if (this.icon === 'outlook') return 'hover:border-blue-300';
            return '';
        }
    },
    methods: {
        handleClick() {
            if (this.refUrl) {
                window.open(this.refUrl, '_blank');
            }
        }
    }
};
</script>