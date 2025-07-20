<template>
    <!-- Footer Contact -->
    <Card class="h-1/5">
        <div>
            <h1 class = "text-xl font-medium text-white text-center">Contact Me!</h1>
            <div class="flex space-between items-center w-full">
                <ContactButton icon="linkedin" color="#0A66C2" refUrl="https://www.linkedin.com/in/justin-lema-riv024/"/>
                <ContactButton icon="instagram" color="#E1306C" refUrl="https://www.instagram.com/lejust_justin/" />
                <ContactButton icon="outlook" color="#0072C6" />
            </div>
        </div>
    </Card>
</template>

<script>
export default {
    name: 'ContactCard'
}
</script>