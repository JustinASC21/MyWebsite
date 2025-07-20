<template>
    <!-- Component card below -->
     <!-- rounded-xl omitted for consistency -->
    <div class="relative drop-shadow-xl w-screen overflow-hidden bg-[#171A21] shadow-2xl">
        <div class="absolute bottom-0 left-1/2 z-0 w-full h-32 -translate-x-1/2 bg-[#AFB3F7] blur-2xl opacity-80 pointer-events-none"></div>
        <div
            class="absolute flex items-center justify-center text-white z-[1] opacity-90 rounded-xl inset-0.5 bg-[#171A21]">
            <slot></slot>
        </div>
        <div class="absolute w-56 h-48 bg-white blur-[50px] -left-1/2 -top-1/2"></div>

    </div>
</template>

<script>
export default {
    name: 'Card',
    props: {
        contentProp: {
            type: String,
            required: false
        }
    }
};
</script>