<template>
    <NuxtLayout>


        <div class="min-h-screen bg-black text-white bg-home bg-center">
            <div class="bg-gradient-to-b from-[#0000008f] to-[#0000008f] min-h-screen pt-16"></div>
        </div>

        <div class="bg-black h-screen"></div>

        <div>
            <section class="h-1/3 md:h-4/5 bg-footer py-20">
                <div class="py-40 mx-4 md:mx-20">
                    <div class="flex justify-center">
                        <p class="text-2xl md:text-2xl lg:text-4xl font-bold text-center text-white">
                            Conheça nossas redes sociais
                        </p>
                    </div>

                    <div class="flex justify-center pb-20 md:pb-44 mt-3">
                        <div class="absolute">
                            <a href="https://www.instagram.com/waaperfumes_/" target="_blank">
                                <IconsInstagramIcon class="size-14 fill-white hover:scale-110 transition duration-150" />
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
</style>