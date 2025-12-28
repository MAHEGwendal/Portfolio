<template>
  <div class="hero bg-iris-950 min-h-screen motion-preset-fade" id="home">
    <div class="hero-content flex-col lg:flex-row-reverse">
      <img src="/images/test.jpg" class="max-w-sm lg:max-w-lg rounded-full shadow-2xl border-2 border-iris-200 p-1 mt-20 lg:mt-0 motion-translate-x-in-[200%] motion-translate-y-in-[-0%] motion-duration-[1s] " />
      <div class="text-center lg:text-left">
        <h1 class="text-xl motion-preset-slide-right motion-duration-[2s] ">Bonjour, je suis</h1>
        <h2 class="text-6xl font-bold mb-4 motion-preset-slide-right motion-duration-[2s] ">Gwendal Mahé !</h2>
        <p class="lg:pr-20 text-2xl motion-preset-slide-right motion-duration-[2s]">
          Étudiant en développement informatique, motivé et curieux, à la recherche d'opportunités pour développer mes
          compétences et gagner en expérience.
        </p>
        <div class="flex justify-center lg:justify-start gap-10 lg:gap-15 mt-5 ">
          <button class="btn bg-iris-200 rounded-xl p-8 text-lg hover:bg-iris-300 hover:shadow-lg hover:shadow-iris-200/50 hover:scale-105 transition motion-preset-expand motion-duration-[2s]" @click="smoothScrollToProjets">Voir mes<br />projets</button>
          <a href="../../public/doc/MAHE_CV.pdf" target="blank"><button class="btn btn-outline rounded-xl border-2 border-iris-200 p-8 text-lg hover:bg-iris-300 hover:shadow-lg hover:shadow-iris-200/50 hover:scale-105 transition motion-preset-expand motion-duration-[2s]">
            Télécharger<br />mon CV
          </button></a>
        </div>

        <div class="flex justify-center lg:justify-start gap-15 mt-8 ">
          <a href="https://github.com/MAHEGwendal" target="blank"><img src="/images/github_logo.webp" alt="Logo Github" class="size-15 lg:size-18 hover:scale-110 transition-transform motion-preset-pop motion-duration-1000" /></a>
          <a href="https://www.linkedin.com/in/gwendal-mahé-72ab202b7/" target="blank"><img src="/images/LinkedIn_logo.png" alt="Logo LinkedIn" class="size-15 lg:size-18 hover:scale-110 transition-transform motion-preset-pop motion-duration-1500" /></a>
          <a href="mailto:mahegwendal8@gmail.com">
          <svg class="size-15 lg:size-18 hover:scale-110 transition-transform motion-preset-pop motion-duration-[2s]" data-slot="icon" fill="#6366f1" viewBox="0 0 24 24" xmlns="http://www.w3.org/2000/svg"
            aria-hidden="true">
            <path d="M1.5 8.67v8.58a3 3 0 0 0 3 3h15a3 3 0 0 0 3-3V8.67l-8.928 5.493a3 3 0 0 1-3.144 0L1.5 8.67Z">
            </path>
            <path
              d="M22.5 6.908V6.75a3 3 0 0 0-3-3h-15a3 3 0 0 0-3 3v.158l9.714 5.978a1.5 1.5 0 0 0 1.572 0L22.5 6.908Z">
            </path>
          </svg>
          </a>
        </div>
      </div>
    </div>
  </div>
</template>

<script setup>
const smoothScrollToProjets = () => {
  const element = document.getElementById('projets');
  if (element) {
    const navHeight = 64;
    const elementPosition = element.getBoundingClientRect().top + window.scrollY - navHeight;
    window.scrollTo({
      top: elementPosition,
      behavior: 'smooth'
    });
  }
};
</script>