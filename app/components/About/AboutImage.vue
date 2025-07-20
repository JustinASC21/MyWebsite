<template>
    <div class="grid min-h-[140px] place-items-center overflow-x-scroll rounded-lg p-6 lg:overflow-visible">
        <figure class="relative w-full h-3/4">
            <img class="object-cover object-center w-full h-full rounded-xl" src="/img/BrooklynCitySkyline.jpeg"
                alt="skyline image" />
            <figcaption
                class="absolute bottom-8 left-2/4 flex w-3/4 -translate-x-2/4 justify-between rounded-xl border border-black bg-white/70 py-4 px-6 shadow-ld shadow-black/5 saturate-200 backdrop-blur-sm">
                <div>
                    <h5 class="text-xl font-medium text-slate-800">
                        Justin Lema
                    </h5>
                    <p class="mt-2 text-slate-600">
                        20 July 2022
                    </p>
                </div>
                <h5 class="text-xl font-medium text-slate-800">
                    Growth
                </h5>
            </figcaption>
        </figure>
    </div>
</template>

<script>
export default {
    name : 'AboutImage'
}
</script>