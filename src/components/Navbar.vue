<template>
  <header
    class="fixed w-full top-0 z-50 bg-iris-900 font-bold lg:motion-translate-x-in-[0%] lg:motion-translate-y-in-[-180%] lg:motion-duration-[2s]">
    <div class="container mx-auto flex justify-between items-center p-3 relative ">
      <!-- Logo -->
      <h1 class="text-3xl text-iris-100">Gwendal Mahé</h1>

      <!-- Desktop Navigation -->
      <nav class="hidden md:flex space-x-6 justify-center items-center text-xl">
        <ul class="menu menu-horizontal px-0 gap-4 text-xl font-bold text-iris-50 ">
          <li><a href="#home" @click="smoothScroll" class=" rounded-xl hover:bg-iris-100/20">Acceuil</a></li>
          <li><a href="#apropos" @click="smoothScroll" class=" rounded-xl hover:bg-iris-100/20" >A propos</a></li>
          <li><a href="#competences" @click="smoothScroll" class=" rounded-xl hover:bg-iris-100/20">Compétences</a></li>
          <li><a href="#projets" @click="smoothScroll" class=" rounded-xl hover:bg-iris-100/20">Projets</a></li>
          <li class="hover:bg-transparent hover:shadow-none">
            <a href="/doc/MAHE_CV_SDV.pdf" target="_blank" class="btn btn-outline text-iris-50 rounded-xl border-2 border-iris-200 p-5 text-sm
               hover:bg-iris-300 hover:shadow-lg hover:shadow-iris-200/50 hover:scale-105 transition">
              Télécharger<br />mon CV
            </a>
          </li>
        </ul>
      </nav>

      <!-- Mobile Menu Button -->
      <button @click="navOpen = !navOpen" class="md:hidden focus:outline-none z-50 relative text-iris-50 "
        aria-label="Toggle navigation">
        <svg v-show="!navOpen" xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" stroke-width="1.5"
          stroke="currentColor" class="w-10 h-10">
          <path stroke-linecap="round" stroke-linejoin="round" d="M3.75 6.75h16.5M3.75 12h16.5m-16.5 5.25h16.5" />
        </svg>
        <svg v-show="navOpen" xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" stroke-width="1.5"
          stroke="currentColor" class="w-10 h-10">
          <path stroke-linecap="round" stroke-linejoin="round" d="M6 18L18 6M6 6l12 12" />
        </svg>
      </button>
    </div>

    <!-- Mobile Navigation -->
    <Transition enter-active-class="transition-transform duration-300 ease-out" enter-from-class="translate-x-full"
      enter-to-class="translate-x-0" leave-active-class="transition-transform duration-300 ease-in"
      leave-from-class="translate-x-0" leave-to-class="translate-x-full">
      <nav v-show="navOpen"
        class="fixed inset-0 bg-iris-900  p-4 transform z-40 justify-center items-center flex flex-col md:hidden text-3xl">
        <ul class="flex flex-col gap-6 items-center w-full text-iris-50">
          <li>
            <a href="#home" @click="navOpen = false; smoothScroll"
              class="motion-preset-expand motion-delay-100 motion-duration-[1s]">Accueil</a>
          </li>
          <li>
            <a href="#apropos" @click="navOpen = false; smoothScroll"
              class="motion-preset-expand motion-delay-100 motion-duration-[1s]">A propos</a>
          </li>
          <li>
            <a href="#competences" @click="navOpen = false; smoothScroll"
              class="motion-preset-expand motion-delay-100 motion-duration-[1s]">Compétences</a>
          </li>
          <li>
            <a href="#projets" @click="navOpen = false; smoothScroll"
              class="motion-preset-expand motion-delay-100 motion-duration-[1s]">Projets</a>
          </li>
          <li> <a href="/doc/MAHE_CV_SDV.pdf" target="_blank" class="btn btn-outline rounded-xl border-2 text-iris-50 border-iris-200 p-5 text-sm
               hover:bg-iris-300 hover:shadow-lg hover:shadow-iris-200/50 hover:scale-105 transition">
              Télécharger<br />mon CV
            </a></li>
        </ul>
      </nav>
    </Transition>
  </header>
</template>

<script setup>
import { ref, onMounted, onUnmounted } from 'vue';

const showScrollTop = ref(false);
const navOpen = ref(false); // État pour gérer l'ouverture/fermeture du menu mobile

const smoothScroll = (e) => {
  e.preventDefault();
  const href = e.target.getAttribute('href');
  const element = document.querySelector(href);
  if (element) {
    const navHeight = 64; // Hauteur de la navbar en pixels
    const elementPosition = element.getBoundingClientRect().top + window.scrollY - navHeight;
    window.scrollTo({
      top: elementPosition,
      behavior: 'smooth'
    });
  }
};

const smoothScrollToContact = () => {
  const element = document.getElementById('contact');
  if (element) {
    const navHeight = 64;
    const elementPosition = element.getBoundingClientRect().top + window.scrollY - navHeight;
    window.scrollTo({
      top: elementPosition,
      behavior: 'smooth'
    });
  }
};

const scrollToTop = () => {
  window.scrollTo({
    top: 0,
    behavior: 'smooth'
  });
};

const handleScroll = () => {
  showScrollTop.value = window.scrollY > 300;
};

onMounted(() => {
  window.addEventListener('scroll', handleScroll);
});

onUnmounted(() => {
  window.removeEventListener('scroll', handleScroll);
});
</script>
