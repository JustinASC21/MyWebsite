<template>
    <Card class="h-2/4">
        <div class = "flex-col items-center">
            <h1 class = "text-xl font-medium text-white text-center pb-10">Experience</h1>
            <div class="w-full grid grid-cols-1 lg:grid-cols-2 gap-8 space-between">
                <ProjectExp :experience="awsExp"></ProjectExp>
                <ProjectExp :experience="ascExp"></ProjectExp>
            </div>
        </div>

    </Card>
</template>

<script setup>
import { ref } from 'vue';

const awsExp = ref({
    company: 'AWS',
    role: 'Software Developer Engineer Intern',
    description: 'Worked alongside AWS Engineers to revamp the team\'s codebase',
    logo: 'aws.svg',
    skills: ['Python', 'NextJS']
});
const ascExp = ref({
    company: 'All Star Code',
    role: 'Teaching Asssitant',
    description: 'Worked alongside a team of passionate instructors in a 6-week coding summer intensive for high school students',
    logo: 'AllStarCodeLogo.png',
    skills: ['Javascript', 'Web Development', 'Git']
})
</script>

<script>
export default {
    name: 'ProjectCard'
}
</script>