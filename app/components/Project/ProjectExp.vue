<template>
    <!-- Project Card -->
    <div
        class="bg-gray-900 rounded-lg p-6 border hover:border-gray-700 transition-all duration-300 relative group">
        <!-- Edit Icon -->
        <div class="absolute top-4 right-4 opacity-0 group-hover:opacity-100 transition-opacity duration-200">
            <button class="text-gray-400 hover:text-white">
                <EditIcon class="h-5 w-5" />
            </button>
        </div>

        <!-- Header with Logo and Title -->
        <div class="flex items-start gap-4 mb-4">
            <div class="flex-shrink-0">
                <img :src="`/img/${experience.logo}`" :alt="experience.company + ' logo'"
                    class="w-16 h-16 rounded-lg object-cover bg-gray-800" />
            </div>
            <div class="flex-1">
                <h3 class="text-xl font-bold text-white mb-1">{{ experience.company }}</h3>
                <p class="text-gray-400 text-sm mb-2">{{ experience.role }}</p>
            </div>
        </div>

        <!-- Description -->
        <p class="text-gray-300 text-sm leading-relaxed mb-6">
            {{ experience.description }}
        </p>

        <!-- Skills/Tags -->
        <div class="flex flex-wrap gap-2">
            <span v-for="skill in experience.skills" :key="skill"
                class="px-4 py-2 bg-[#9095F7] hover:bg-purple-700 text-white text-sm rounded-full transition-colors duration-200 cursor-default">
                {{ skill }}
            </span>
        </div>
    </div>
</template>

<script setup>
import { EditIcon } from 'lucide-vue-next'

const props = defineProps({
    experience: {
        type: Object,
        required: true,
        default: () => ({
            company: '',
            role: '',
            description: '',
            logo: '',
            skills: []
        })
    }
})

// onMounted(() => {
//     console.log(props.experience.logo)
// })
</script>
