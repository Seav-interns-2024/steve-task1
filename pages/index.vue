<template>


    <div class="bg-[#f7d0b6] py-20">
        <div class="max-w-screen-lg mx-auto flex justify-between items-center">
            <div class="max-w-xl">
                <h2 class="font-black text-sky-950 text-3xl mb-4">A Societal Mission</h2>
                <p class="text-base text-sky-950">Stanford was founded almost 150 years ago on a bedrock of societal
                    purpose. Our mission is to contribute to the world by educating students for lives of leadership and
                    contribution with integrity; advancing fundamental knowledge and cultivating creativity; leading in
                    pioneering research for effective clinical therapies; and accelerating solutions and amplifying
                    their impact.</p>
            </div>
        </div>
    </div>
    <div class="py-12 relative overflow-hidden bg-white">
        <div class="grid grid-cols-2 max-w-screen-lg mx-auto">
            <div class="w-full flex flex-col items-end pr-16">
                <h2 class="text-[#64618C] font-bold text-2xl max-w-xs text-right mb-12 mt-10">Stanford president</h2>
                <div class="h-full mt-auto overflow-hidden relative">
                    <img src="assets/Jonathan-Levin-Portrait-Med.jpg" class="h-full w-full object-contain" alt="">
                </div>
            </div>

            <div
                class="py-20 bg-slate-100 relative before:absolute before:h-full before:w-screen before:bg-sky-950 before:top-0 before:left-0">
                <div class="relative z-20 pl-12">
                    <h2 class="text-[#f7d0b6] font-black text-5xl leading-snug mb-10">Jonathan Levin
                    </h2>
                    <p class="text-white text-sm">
                        Jonathan Levin, a distinguished economist and Stanford alumnus who has led the Stanford Graduate
                        School of Business as dean for the last eight years, has been appointed the next president of
                        Stanford University, the Board of Trustees announced today.
                    </p>
                    <button @click="Show"
                        class="mt-8 text-white uppercase py-3 text-sm px-10 border border-white hover:bg-white hover:bg-opacity-10">Read
                        full story</button>
                </div>
            </div>
        </div>
    </div>

    <div class="py-4 relative overflow-hidden bg-white">
        <div class="grid grid-cols-2 max-w-screen-lg mx-auto">


            <div
                class="py-20 bg-slate-100 relative before:absolute before:h-full before:w-screen before:bg-[#f7d0b6] before:top-0 before:right-0">
                <div class="relative z-20 pl-12">
                    <h2 class="text-sky-950 font-black text-5xl leading-snug mb-10">Undergraduate Education
                    </h2>
                    <p class="text-sky-950 text-sm">
                        Rich learning experiences that provide a broad liberal arts foundation and deep subject-area
                        expertise
                    </p>
                    <button @click="Show"
                        class="mt-8 text-white uppercase py-3 text-sm px-10 border border-white hover:bg-white hover:bg-opacity-10">Graduate
                        Education</button>
                </div>
            </div>
            <div class="w-full flex flex-col pl-16">
                <h2 class="text-[#64618C] font-bold text-2xl max-w-xs text-left mb-12 mt-10">Academic Information
                </h2>
                <div class="h-full mt-auto overflow-hidden relative">
                    <img src="assets/Grayson.webp" class="h-full w-full object-contain" alt="">
                </div>
            </div>

        </div>
    </div>

    <div class="py-12 relative overflow-hidden bg-white">
        <div class="grid grid-cols-2 max-w-screen-lg mx-auto">
            <div class="w-full flex flex-col items-end pr-16">
                <h2 class="text-[#64618C] font-bold text-2xl max-w-xs text-right mb-12 mt-10"></h2>
                <div class="h-full mt-auto overflow-hidden relative">
                    <img src="assets/Hopkins.webp" class="h-full w-full object-contain" alt="">
                </div>
            </div>

            <div
                class="py-20 bg-slate-100 relative before:absolute before:h-full before:w-screen before:bg-sky-950 before:top-0 before:left-0">
                <div class="relative z-20 pl-12">
                    <h2 class="text-[#f7d0b6] font-black text-5xl leading-snug mb-10">Graduate Education
                    </h2>
                    <p class="text-white text-sm">
                        Unsurpassed opportunities to participate in the advancement of entire fields of knowledge
                    </p>
                    <button @click="Show"
                        class="mt-8 text-white uppercase py-3 text-sm px-10 border border-white hover:bg-white hover:bg-opacity-10">Graduate
                        Education</button>
                </div>
            </div>
        </div>
    </div>
</template>


<script>
export default {
    methods: {
        Show() {
            alert('Go to Stanford University Official Website.')
        }
    }
}
</script>

<style></style>