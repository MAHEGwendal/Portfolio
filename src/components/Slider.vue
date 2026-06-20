<template>
    <h2 class="text-4xl font-bold text-iris-100 text-left my-8 pl-12">
        - Mes projets
    </h2>
    <p class="pl-12 text-sm text-iris-50/70">
        Une démo est disponible si vous cliquez sur l'image.
    </p>

    <div class="w-full flex flex-col items-center justify-center mt-5">
        <!-- Slider -->
        <div class="relative flex items-center justify-center" @mouseenter="pauseAutoPlay" @mouseleave="startAutoPlay">
            <div class="flex justify-center items-center gap-6 overflow-visible w-full px-20">

                <!-- Slide Gauche -->
                <div
                    class="flex-shrink-0 w-70 h-32 opacity-50 scale-75 transition-all duration-500 cursor-pointer hover:opacity-80 md:block hidden"
                    @click="prev"
                >
                    <img :src="slides[getPrevIndex()].src" :alt="slides[getPrevIndex()].alt"
                        class="w-full h-full object-cover rounded-lg" />
                </div>

                <!-- Slide Centrale -->
                <div
                    :class="[
                        'flex-shrink-0 w-90 h-50 md:w-150 md:h-70 relative transition-all rounded-2xl duration-500 transform group hover:scale-105 hover:shadow-xl hover:shadow-iris-100/50 ',
                        animatePop ? 'motion-preset-pop motion-duration-[1s]' : ''
                    ]"
                    @animationend="animatePop = false"
                >
                    <a v-if="slides[currentIndex].link" :href="slides[currentIndex].link" target="_blank"
                        rel="noopener noreferrer" class="cursor-pointer">
                        <img :src="slides[currentIndex].src" :alt="slides[currentIndex].alt"
                            class="w-full h-full object-cover rounded-2xl shadow-xl shadow-iris-100/10 border border-iris-500 "
                            loading="lazy" />
                    </a>
                    <img v-else :src="slides[currentIndex].src" :alt="slides[currentIndex].alt"
                        class="w-full h-full object-cover rounded-2xl shadow-2xl border border-iris-500 " />

                    <div
                        class="absolute bottom-0 left-0 right-0 bg-gradient-to-t from-black to-transparent p-4 rounded-b-2xl ">
                        <h3 class="text-white text-xl font-bold">
                            {{ slides[currentIndex].name }}
                        </h3>
                        <p class="text-gray-300 text-sm mt-2">
                            {{ slides[currentIndex].description }}
                        </p>
                    </div>
                </div>

                <!-- Slide Droite -->
                <div
                    class="flex-shrink-0 w-70 h-32 opacity-50 scale-75 transition-all duration-500 cursor-pointer hover:opacity-80 md:block hidden"
                    @click="next"
                >
                    <img :src="slides[getNextIndex()].src" :alt="slides[getNextIndex()].alt"
                        class="w-full h-full object-cover rounded-lg" />
                </div>

            </div>
        </div>

        <!-- Contrôles -->
        <div class="flex justify-center items-center gap-4 mt-8">

            <!-- Bouton Précédent -->
            <button @click="prev" class="rounded-full p-2 mr-8 transition-all duration-300 hover:scale-110 cursor-pointer">
                <svg class="w-5 h-5 text-iris-100" fill="none" stroke="currentColor" viewBox="0 0 24 24">
                    <path stroke-linecap="round" stroke-linejoin="round" stroke-width="4" d="M15 19l-7-7 7-7" />
                </svg>
            </button>

            <!-- Indicateurs -->
            <div class="flex gap-2">
                <button
                    v-for="(slide, index) in slides"
                    :key="index"
                    @click="goToSlide(index)"
                    :class="[
                        'h-2 rounded-full transition-all duration-300 cursor-pointer',
                        index === currentIndex ? 'bg-white w-8' : 'bg-gray-500 w-2'
                    ]"
                />
            </div>

            <!-- Bouton Suivant -->
            <button @click="next" class="rounded-full p-2 ml-8 transition-all duration-300 hover:scale-110 cursor-pointer">
                <svg class="w-5 h-5 text-iris-100" fill="none" stroke="currentColor" viewBox="0 0 24 24">
                    <path stroke-linecap="round" stroke-linejoin="round" stroke-width="4" d="M9 5l7 7-7 7" />
                </svg>
            </button>
        </div>
    </div>
</template>

<script setup>
import { ref, watch, onMounted, onUnmounted } from 'vue';

const currentIndex = ref(0);
const animatePop = ref(true); // Ajouté
let autoPlayInterval = null;
const AUTO_PLAY_DELAY = 8000;

const slides = ref([
    {
        src: '/images/InstantGeek.png',
        alt: 'Instant Geek',
        name: 'Instant Geek',
        link: 'https://instantgeek.netlify.app',
        description: 'Faux site de vente de clés de jeux'
    },
        {
        src: '/images/Dawan_Skills.png',
        alt: 'Dawan skills',
        name: 'Dawan skills',
        link: 'https://skills.dawan.fr/#/',
        description: "Site d'apprentissage via des quiz"
    },
    {
        src: '/images/COE33.png',
        alt: 'Clair Obscur',
        name: 'Clair Obscur',
        link: 'https://mahegwendal.github.io/Clair_Obscur_fake_store_front/',
        description: 'Une fois par an, la Peintresse se réveille...'
    },
    {
        src: '/images/Pokemon.png',
        alt: 'Shiny Encounter',
        name: 'Shiny Encounter',
        link: 'https://mahegwendal.github.io/shiny_counter.github.io/',
        description: 'Outil pour la chasse au Pokémon chromatique'
    },
    {
        src: '/images/Resto.png',
        alt: 'Le Comptoir',
        name: 'Le Comptoir',
        link: 'https://mahegwendal.github.io/Site_resto_test.github.io/',
        description: "Site test sur le thème d'un restaurant"
    }
]);

const getPrevIndex = () =>
    (currentIndex.value - 1 + slides.value.length) % slides.value.length;

const getNextIndex = () =>
    (currentIndex.value + 1) % slides.value.length;

const goToSlide = (index) => {
    currentIndex.value = index;
    triggerPop();
    startAutoPlay();
};

const next = () => {
    goToSlide(getNextIndex());
};

const prev = () => {
    goToSlide(getPrevIndex());
};

function triggerPop() {
    animatePop.value = false;
    // Force le reflow pour relancer l'animation
    void document.body.offsetHeight;
    animatePop.value = true;
}

// Relance l'animation à chaque changement de currentIndex (au cas où)
watch(currentIndex, () => {
    triggerPop();
});

// Autoplay
const startAutoPlay = () => {
    stopAutoPlay();
    autoPlayInterval = setInterval(next, AUTO_PLAY_DELAY);
};

const stopAutoPlay = () => {
    if (autoPlayInterval) {
        clearInterval(autoPlayInterval);
        autoPlayInterval = null;
    }
};

const pauseAutoPlay = () => stopAutoPlay();

onMounted(startAutoPlay);
onUnmounted(stopAutoPlay);
</script>
