<script setup>
import { ref, onMounted, onBeforeUnmount } from 'vue';

const menu = ref(false)

const isHidden = ref(false);
let lastScrollTop = 0;

const isNavbarOpaque = ref(false);

const handleScroll = () => {
    const scrollThreshold = 100;
    isNavbarOpaque.value = window.scrollY > scrollThreshold;

    const currentScrollTop = window.pageYOffset || document.documentElement.scrollTop;

    if (currentScrollTop > lastScrollTop) {
        // Scroll para baixo
        isHidden.value = true;
    } else {
        // Scroll para cima
        isHidden.value = false;
    }

    lastScrollTop = currentScrollTop <= 0 ? 0 : currentScrollTop;
};

onMounted(() => {
    window.addEventListener('scroll', handleScroll);
});

onBeforeUnmount(() => {
    window.removeEventListener('scroll', handleScroll);
});
</script>

<template>
    <nav :class="{ 'border-b border-b-black bg-black': isNavbarOpaque, '-translate-y-full ease-in': isHidden, '-translate-y-0 ease-out': !isHidden }"
        class="fixed top-0 z-30 w-full transition duration-700 ease-in-out">
        <div class="flex flex-wrap items-center justify-between max-w-screen-2xl px-1 lg:px-4 py-3 lg:py-0 mx-auto">
            <NuxtLink to="/" class="flex items-center gap-1 transition duration-700 ease-in-out text-white">
                <img src="../assets/logo-nobg.png" class="h-8 w-12 object-cover">
                <span
                    class="self-center text-xl font-semibold lg:text-2xl whitespace-nowrap traced-black text-secondary">WAA
                    Parfum</span>
            </NuxtLink>

            <div class="lg:order-3">
                <a href="https://wa.me/+55859" target="_blank">
                    <Button>Compre Agora</Button>
                </a>
            </div>

            <div class="flex lg:order-2">
                <button @click="menu = !menu" :class="{ 'opened': menu }"
                    class="inline-flex items-center stroke-white justify-center w-10 h-10 p-1 text-sm rounded-lg lg:hidden transition duration-700 ease-in-out">
                    <svg width="100" height="100" viewBox="0 0 100 100">
                        <path class="line line1"
                            d="M 20,29.000046 H 80.000231 C 80.000231,29.000046 94.498839,28.817352 94.532987,66.711331 94.543142,77.980673 90.966081,81.670246 85.259173,81.668997 79.552261,81.667751 75.000211,74.999942 75.000211,74.999942 L 25.000021,25.000058" />
                        <path class="line line2" d="M 20,50 H 80" />
                        <path class="line line3"
                            d="M 20,70.999954 H 80.000231 C 80.000231,70.999954 94.498839,71.182648 94.532987,33.288669 94.543142,22.019327 90.966081,18.329754 85.259173,18.331003 79.552261,18.332249 75.000211,25.000058 75.000211,25.000058 L 25.000021,74.999942" />
                    </svg>
                </button>
            </div>

            <div :class="{ 'lg:block': menu, 'hidden lg:block': !menu }" class="w-full lg:w-auto lg:order-1"
                id="navbar-default">
                <ul :class="{ 'bg-black': isNavbarOpaque, '': !isNavbarOpaque }"
                    class="flex flex-col transition duration-700 ease-in-out p-4 mt-4 font-medium border border-gray-100 rounded-lg lg:p-0 lg:flex-row lg:space-x-14 lg:mt-0 lg:border-0 lg:bg-transparent">
                    <a href="#Sobre">
                        <li>
                            <button class="block py-2 pl-3 pr-4 rounded lg:border-0 lg:py-5 text-white">
                                Sobre
                            </button>
                        </li>
                    </a>
                    <a href="#Produtos">
                        <li>
                            <button class="block py-2 pl-3 pr-4 rounded lg:border-0 lg:py-5 text-white">
                                Produtos
                            </button>
                        </li>
                    </a>
                    <a href="#Contato">
                        <li>
                            <button class="block py-2 pl-3 pr-4 rounded lg:border-0 lg:py-5 text-white">
                                Contato
                            </button>
                        </li>
                    </a>
                </ul>
            </div>
        </div>
    </nav>

    <div>
        <slot />
    </div>

    <footer class="bg-black shadow">
        <div class="w-full max-w-screen-xl mx-auto p-4 md:py-8">
            <div class="sm:flex sm:items-center sm:justify-between">
                <a href="/" class="flex items-center mb-4 sm:mb-0 space-x-3 rtl:space-x-reverse">
                    <img src="../assets/logo-nobg.png" class="h-20" alt="WAA Parfum Logo" />
                    <span class="self-center text-2xl font-semibold whitespace-nowrap text-white">WAA Parfum</span>
                </a>
                <ul
                    class="flex flex-wrap items-center mb-6 text-sm font-medium text-white sm:mb-0">
                    <li>
                        <a href="#Sobre" class="hover:underline me-4 md:me-6">Sobre</a>
                    </li>
                    <li>
                        <a href="#Produtos" class="hover:underline me-4 md:me-6">Produtos</a>
                    </li>
                    <li>
                        <a href="#Contato" class="hover:underline me-4 md:me-6">Contato</a>
                    </li>
                </ul>
            </div>
            <hr class="my-6 border-gray-200 sm:mx-auto lg:my-8" />
            <span class="block text-sm text-gray-500 sm:text-center">© 2024 <a
                    href="/" class="hover:underline">WAA Parfum™</a>. All Rights Reserved.</span>
        </div>
    </footer>
</template>

<style>
.menu {
    background-color: transparent;
    border: none;
    cursor: pointer;
    display: flex;
    padding: 0;
}

.line {
    fill: none;
    stroke-width: 7;
    transition: stroke-dasharray 500ms cubic-bezier(0.4, 0, 0.2, 1),
        stroke-dashoffset 500ms cubic-bezier(0.4, 0, 0.2, 1);
}

.line1 {
    stroke-dasharray: 60 207;
    stroke-width: 7;
}

.line2 {
    stroke-dasharray: 60 60;
    stroke-width: 7;
}

.line3 {
    stroke-dasharray: 60 207;
    stroke-width: 7;
}

.opened .line1 {
    stroke-dasharray: 90 207;
    stroke-dashoffset: -134;
    stroke-width: 6;
}

.opened .line2 {
    stroke-dasharray: 1 60;
    stroke-dashoffset: -30;
    stroke-width: 6;
}

.opened .line3 {
    stroke-dasharray: 90 207;
    stroke-dashoffset: -134;
    stroke-width: 6;
}

.v-enter-active,
.v-leave-active {
    transition: opacity 0.5s ease;
}

.v-enter-from,
.v-leave-to {
    opacity: 0;
}
</style>