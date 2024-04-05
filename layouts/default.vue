<template>
    <div>
        <header class="shadow-sm bg-black h-20">
            <nav class="container mx-auto pl-4 pr-4 flex justify-between items-center h-full">
                <NuxtLink to="/" class="font-serif text-red-400  ">Stanford University</NuxtLink>
                <ul class="flex gap-4 text-white font-serif py-1 px-3 rounded">
                
                    <li class="hover:scale-90 hover:bg-black transition duration-200 ease-in-out">
                        <NuxtLink to="/register">Register</NuxtLink>
                    </li>
                    <li class="hover:scale-90 hover:bg-black transition duration-200 ease-in-out">
                        <NuxtLink to="/student">Student</NuxtLink>
                    </li>
                    <li class="hover:scale-90 hover:bg-black transition duration-200 ease-in-out">
                        <NuxtLink to="/alumni">Alumni</NuxtLink>
                    </li>
                </ul>
            </nav>
        </header>
    </div>
    <div class="container mx-auto p-4">
        <slot />
    </div>
</template>
<script>

</script>
<style scoped></style>
