<template>
    <NuxtLayout>
        <div class="min-h-screen bg-black text-white bg-home bg-center">
            <div class="bg-gradient-to-b from-[#000000a4] to-[#000000a4] min-h-screen">
                <div class="flex flex-col lg:flex-row justify-center lg:justify-evenly items-center h-screen">
                    <div class="order-2 lg:order-1 text-center">
                        <p class="text-4xl lg:text-5xl font-bold font-playfair underline">WAA Parfum</p>
                        <p class="lg:text-lg mx-3 lg:mx-0">Perfume é mais do que cosmético, é memória. 🍃🧠</p>

                        <div class="flex justify-center">
                            <a href="https://www.instagram.com/waaperfumes_/" target="_blank">
                                <IconsInstagramIcon
                                    class="fill-white size-12 hover:scale-110 transition duration-150" />
                            </a>
                        </div>
                    </div>
                    <div class="order-1 lg:order-2">
                        <img src="../assets/logo-nobg.png" class="h-72 object-cover" alt="">
                    </div>
                </div>
            </div>
        </div>

        <div class="bg-black h-screen"></div>

        <div>
            <section class="h-1/3 md:h-4/5 bg-footer py-20">
                <div class="py-40 mx-4 md:mx-20">
                    <div class="flex justify-center">
                        <p class="text-2xl md:text-2xl font-playfair lg:text-4xl font-bold text-center text-white">
                            Conheça nossas redes sociais
                        </p>
                    </div>

                    <div class="flex justify-center pb-20 md:pb-44 mt-3">
                        <div class="absolute">
                            <a href="https://www.instagram.com/waaperfumes_/" target="_blank">
                                <IconsInstagramIcon
                                    class="size-14 fill-white hover:scale-110 transition duration-150" />
                            </a>
                        </div>
                    </div>
                </div>
            </section>
        </div>


        <!--Test
        <div class="min-h-screen bg-green-600">
            <img src="../assets/logo-nobg.png" class="" alt="">
        </div>
        -->
    </NuxtLayout>
</template>

<style scoped>
.bg-home {
    background-image: url('../assets/home.jpeg');
}

.bg-footer {
    background-size: cover;
    background-position: center;
    width: 100%;
    background-image: linear-gradient(#8a8a8a80, #9333ea), url('../assets/footer.jpeg');
    background-repeat: no-repeat;
}

.font-playfair {
    font-family: 'Playfair Display', serif;
}
</style>