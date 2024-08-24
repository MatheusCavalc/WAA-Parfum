<template>
    <Title>WAA Parfum</Title>
    <NuxtLayout>
        <div class="min-h-screen bg-black text-white bg-home bg-center bg-cover bg-no-repeat">
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

        <div class="bg-black min-h-screen">
            <a id="Produtos" />
            <p class="py-8 text-4xl font-bold text-white text-center">Produtos</p>

            <div class="bg-black lg:flex gap-8 lg:justify-evenly items-center px-10 py-20 lg:py-20 lg:px-36">
                <div class="h-full">
                    <img class="w-96 object-cover rounded-sm" src="../assets/coco_noir.jpeg" alt="">
                </div>

                <div class="mt-8 text-white lg:w-1/2">
                    <h2 class="text-2xl font-playfair font-semibold lg:text-4xl">COCO NOIR</h2>
                    <p class="mt-6">COCO NOIR personifica uma afirmação paradoxal. Atribuindo à escuridão uma função
                        essencial: revelar a feminilidade em todo o seu esplendor.</p>

                    <p class="my-6 text-xl font-bold">Preço: R$ XX,XX</p>

                    <Button>Pedir</Button>
                </div>
            </div>

            <div class="bg-black lg:flex gap-8 lg:justify-evenly items-center px-10 py-20 lg:py-20 lg:px-36">
                <div class="h-full">
                    <img class="w-96 object-cover rounded-sm" src="../assets/jadore.jpeg" alt="">
                </div>

                <div class="mt-8 text-white lg:w-1/2">
                    <h2 class="text-2xl font-playfair font-semibold lg:text-4xl">J'adore</h2>
                    <p class="mt-6">Um dos perfumes mais utilizados por mulheres sofisticadas, J'adore é a fragrância
                        que representa a Feminilidade Absoluta.</p>

                    <p class="my-6 text-xl font-bold">Preço: R$ XX,XX</p>

                    <Button>Pedir</Button>
                </div>
            </div>
        </div>

        <div>
            <a id="Contato" />
            <section class="h-1/3 md:h-4/5 bg-footer bg-center bg-cover bg-no-repeat py-20">
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
    </NuxtLayout>
</template>
