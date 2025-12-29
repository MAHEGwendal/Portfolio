<template>
  <div>
    <div class="flex flex-col md:flex-row p-4 md:p-10 gap-6 md:gap-10">
      <div class="md:flex-1">
        <h2 class="text-4xl font-bold mb-5 text-iris-100 md:text-left motion-preset-slide-up motion-delay-200">- A propos</h2>
        <p class="text-lg mb-5 text-iris-50 text-center md:text-left">
          Je m'appelle Gwendal Mahé, développeur web passionné et autodidacte.<br />
          Actuellement en Titre Professionnel Concepteur Développeur d'Applications Java chez Dawan Nantes, je développe
          mes compétences en conception et développement d'applications, aussi bien côté backend que frontend.<br />
          <br />
          Curieux et motivé, j'aime apprendre à travers des projets concrets et relever de nouveaux défis techniques. Je
          suis actuellement à la recherche d'une alternance afin de mettre en pratique mes connaissances et évoluer dans
          un environnement professionnel stimulant.
        </p>
        <div class="flex justify-center md:justify-start">
          <a href="/doc/MAHE_CV.pdf" target="blank"><button class="btn btn-outline rounded-xl border-2 border-iris-200 p-8 text-lg hover:bg-iris-300 hover:shadow-lg hover:shadow-iris-200/50 hover:scale-105 transition">
            Télécharger<br />mon CV
          </button></a>
        </div>
      </div>
      <div class="md:flex-1 mt-8 md:mt-0">
        <div class="grid grid-cols-2 gap-5">
          <!-- Code Propre -->
          <div class="border border-iris-400/50 rounded-2xl p-6 bg-iris-950/50">
            <svg class="w-8 h-8 text-iris-400 mb-4 mx-auto lg:ml-0" fill="none" stroke="currentColor" viewBox="0 0 24 24"
              xmlns="http://www.w3.org/2000/svg">
              <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2"
                d="M10 20l4-16m4 4l4 4-4 4M6 16l-4-4 4-4" />
            </svg>
            <h3 class="text-white font-bold text-lg mb-2">Code Propre</h3>
            <p class="text-iris-200 text-sm">Écriture d'un code maintenable, lisible et évolutif</p>
          </div>
          <!-- Application Web -->
          <div class="border border-iris-400/50 rounded-2xl p-6 bg-iris-950/50">
            <svg class="w-8 h-8 text-iris-400 mb-4 mx-auto lg:ml-0" fill="currentColor" viewBox="0 0 24 24"
              xmlns="http://www.w3.org/2000/svg" aria-hidden="true">
              <path clip-rule="evenodd" fill-rule="evenodd"
                d="M2.25 5.25a3 3 0 0 1 3-3h13.5a3 3 0 0 1 3 3V15a3 3 0 0 1-3 3h-3v.257c0 .597.237 1.17.659 1.591l.621.622a.75.75 0 0 1-.53 1.28h-9a.75.75 0 0 1-.53-1.28l.621-.622a2.25 2.25 0 0 0 .659-1.59V18h-3a3 3 0 0 1-3-3V5.25Zm1.5 0v7.5a1.5 1.5 0 0 0 1.5 1.5h13.5a1.5 1.5 0 0 0 1.5-1.5v-7.5a1.5 1.5 0 0 0-1.5-1.5H5.25a1.5 1.5 0 0 0-1.5 1.5Z">
              </path>
            </svg>
            <h3 class="text-white font-bold text-lg mb-2">Applications web</h3>
            <p class="text-iris-200 text-sm">Développement d'applications web full stack</p>
          </div>
          <!-- Autonomie & adaptabilité -->
          <div class="border border-iris-400/50 rounded-2xl p-6 bg-iris-950/50">
            <svg class="w-8 h-8 text-iris-400 mb-4 mx-auto lg:ml-0" fill="currentColor" viewBox="0 0 24 24"
              xmlns="http://www.w3.org/2000/svg" aria-hidden="true">
              <path clip-rule="evenodd" fill-rule="evenodd"
                d="M12 2.25c-5.385 0-9.75 4.365-9.75 9.75s4.365 9.75 9.75 9.75 9.75-4.365 9.75-9.75S17.385 2.25 12 2.25Zm-2.625 6c-.54 0-.828.419-.936.634a1.96 1.96 0 0 0-.189.866c0 .298.059.605.189.866.108.215.395.634.936.634.54 0 .828-.419.936-.634.13-.26.189-.568.189-.866 0-.298-.059-.605-.189-.866-.108-.215-.395-.634-.936-.634Zm4.314.634c.108-.215.395-.634.936-.634.54 0 .828.419.936.634.13.26.189.568.189.866 0 .298-.059.605-.189.866-.108.215-.395.634-.936.634-.54 0-.828-.419-.936-.634a1.96 1.96 0 0 1-.189-.866c0-.298.059-.605.189-.866Zm2.023 6.828a.75.75 0 1 0-1.06-1.06 3.75 3.75 0 0 1-5.304 0 .75.75 0 0 0-1.06 1.06 5.25 5.25 0 0 0 7.424 0Z">
              </path>
            </svg>
            <h3 class="text-white font-bold text-lg mb-2">Autonomie & adaptabilité</h3>
            <p class="text-iris-200 text-sm">Capacité à s'adapter rapidement à de nouveaux environnements</p>
          </div>
          <!-- Design Responsive -->
          <div class="border border-iris-400/50 rounded-2xl p-6 bg-iris-950/50">
            <svg class="w-8 h-8 text-iris-400 mb-4 mx-auto lg:ml-0" fill="currentColor" viewBox="0 0 24 24"
              xmlns="http://www.w3.org/2000/svg" aria-hidden="true">
              <path d="M10.5 18.75a.75.75 0 0 0 0 1.5h3a.75.75 0 0 0 0-1.5h-3Z"></path>
              <path clip-rule="evenodd" fill-rule="evenodd"
                d="M8.625.75A3.375 3.375 0 0 0 5.25 4.125v15.75a3.375 3.375 0 0 0 3.375 3.375h6.75a3.375 3.375 0 0 0 3.375-3.375V4.125A3.375 3.375 0 0 0 15.375.75h-6.75ZM7.5 4.125C7.5 3.504 8.004 3 8.625 3H9.75v.375c0 .621.504 1.125 1.125 1.125h2.25c.621 0 1.125-.504 1.125-1.125V3h1.125c.621 0 1.125.504 1.125 1.125v15.75c0 .621-.504 1.125-1.125 1.125h-6.75A1.125 1.125 0 0 1 7.5 19.875V4.125Z">
              </path>
            </svg>
            <h3 class="text-white font-bold text-lg mb-2">Design responsive</h3>
            <p class="text-iris-200 text-sm">Approche mobile-first orientée UI/UX</p>
          </div>
        </div>
      </div>
    </div>

    <h2 class="text-4xl font-bold  p-10 text-iris-100">- Formation</h2>
    <div class="grid grid-cols-1 md:grid-cols-3 gap-4 w-full px-4 md:px-10 pb-10">
      <!-- Formation 1 -->
      <div
        class="border border-iris-400/50 rounded-2xl p-6 bg-iris-950/50 hover:shadow-xl hover:shadow-iris-50/10 hover:scale-101 transition">
        <svg class="w-8 h-8 text-iris-400 mb-4" fill="currentColor" viewBox="0 0 24 24"
          xmlns="http://www.w3.org/2000/svg" aria-hidden="true">
          <path
            d="M11.7 2.805a.75.75 0 0 1 .6 0A60.65 60.65 0 0 1 22.83 8.72a.75.75 0 0 1-.231 1.337 49.948 49.948 0 0 0-9.902 3.912l-.003.002c-.114.06-.227.119-.34.18a.75.75 0 0 1-.707 0A50.88 50.88 0 0 0 7.5 12.173v-.224c0-.131.067-.248.172-.311a54.615 54.615 0 0 1 4.653-2.52.75.75 0 0 0-.65-1.352 56.123 56.123 0 0 0-4.78 2.589 1.858 1.858 0 0 0-.859 1.228 49.803 49.803 0 0 0-4.634-1.527.75.75 0 0 1-.231-1.337A60.653 60.653 0 0 1 11.7 2.805Z">
          </path>
          <path
            d="M13.06 15.473a48.45 48.45 0 0 1 7.666-3.282c.134 1.414.22 2.843.255 4.284a.75.75 0 0 1-.46.711 47.87 47.87 0 0 0-8.105 4.342.75.75 0 0 1-.832 0 47.87 47.87 0 0 0-8.104-4.342.75.75 0 0 1-.461-.71c.035-1.442.121-2.87.255-4.286.921.304 1.83.634 2.726.99v1.27a1.5 1.5 0 0 0-.14 2.508c-.09.38-.222.753-.397 1.11.452.213.901.434 1.346.66a6.727 6.727 0 0 0 .551-1.607 1.5 1.5 0 0 0 .14-2.67v-.645a48.549 48.549 0 0 1 3.44 1.667 2.25 2.25 0 0 0 2.12 0Z">
          </path>
          <path
            d="M4.462 19.462c.42-.419.753-.89 1-1.395.453.214.902.435 1.347.662a6.742 6.742 0 0 1-1.286 1.794.75.75 0 0 1-1.06-1.06Z">
          </path>
        </svg>
        <h3 class="text-white font-bold text-lg mb-2">Titre Professionnel Concepteur Développeur d'Applications</h3>
        <p class="text-iris-200 text-sm">Dawan, Nantes | 2025-2026</p>
      </div>

      <!-- Formation 2 -->
      <div
        class="border border-iris-400/50 rounded-2xl p-6 bg-iris-950/50 hover:shadow-xl hover:shadow-iris-50/10 hover:scale-101 transition">
        <svg class="w-8 h-8 text-iris-400 mb-4" fill="currentColor" viewBox="0 0 24 24"
          xmlns="http://www.w3.org/2000/svg" aria-hidden="true">
          <path
            d="M11.7 2.805a.75.75 0 0 1 .6 0A60.65 60.65 0 0 1 22.83 8.72a.75.75 0 0 1-.231 1.337 49.948 49.948 0 0 0-9.902 3.912l-.003.002c-.114.06-.227.119-.34.18a.75.75 0 0 1-.707 0A50.88 50.88 0 0 0 7.5 12.173v-.224c0-.131.067-.248.172-.311a54.615 54.615 0 0 1 4.653-2.52.75.75 0 0 0-.65-1.352 56.123 56.123 0 0 0-4.78 2.589 1.858 1.858 0 0 0-.859 1.228 49.803 49.803 0 0 0-4.634-1.527.75.75 0 0 1-.231-1.337A60.653 60.653 0 0 1 11.7 2.805Z">
          </path>
          <path
            d="M13.06 15.473a48.45 48.45 0 0 1 7.666-3.282c.134 1.414.22 2.843.255 4.284a.75.75 0 0 1-.46.711 47.87 47.87 0 0 0-8.105 4.342.75.75 0 0 1-.832 0 47.87 47.87 0 0 0-8.104-4.342.75.75 0 0 1-.461-.71c.035-1.442.121-2.87.255-4.286.921.304 1.83.634 2.726.99v1.27a1.5 1.5 0 0 0-.14 2.508c-.09.38-.222.753-.397 1.11.452.213.901.434 1.346.66a6.727 6.727 0 0 0 .551-1.607 1.5 1.5 0 0 0 .14-2.67v-.645a48.549 48.549 0 0 1 3.44 1.667 2.25 2.25 0 0 0 2.12 0Z">
          </path>
          <path
            d="M4.462 19.462c.42-.419.753-.89 1-1.395.453.214.902.435 1.347.662a6.742 6.742 0 0 1-1.286 1.794.75.75 0 0 1-1.06-1.06Z">
          </path>
        </svg>
        <h3 class="text-white font-bold text-lg mb-2">POE frontend</h3>
        <p class="text-iris-200 text-sm">Dawan, Nantes | 2025</p>
      </div>

      <!-- Formation 3 -->
      <div
        class="border border-iris-400/50 rounded-2xl p-6 bg-iris-950/50 hover:shadow-xl hover:shadow-iris-50/10 hover:scale-101 transition">
        <svg class="w-8 h-8 text-iris-400 mb-4" fill="currentColor" viewBox="0 0 24 24"
          xmlns="http://www.w3.org/2000/svg" aria-hidden="true">
          <path
            d="M11.7 2.805a.75.75 0 0 1 .6 0A60.65 60.65 0 0 1 22.83 8.72a.75.75 0 0 1-.231 1.337 49.948 49.948 0 0 0-9.902 3.912l-.003.002c-.114.06-.227.119-.34.18a.75.75 0 0 1-.707 0A50.88 50.88 0 0 0 7.5 12.173v-.224c0-.131.067-.248.172-.311a54.615 54.615 0 0 1 4.653-2.52.75.75 0 0 0-.65-1.352 56.123 56.123 0 0 0-4.78 2.589 1.858 1.858 0 0 0-.859 1.228 49.803 49.803 0 0 0-4.634-1.527.75.75 0 0 1-.231-1.337A60.653 60.653 0 0 1 11.7 2.805Z">
          </path>
          <path
            d="M13.06 15.473a48.45 48.45 0 0 1 7.666-3.282c.134 1.414.22 2.843.255 4.284a.75.75 0 0 1-.46.711 47.87 47.87 0 0 0-8.105 4.342.75.75 0 0 1-.832 0 47.87 47.87 0 0 0-8.104-4.342.75.75 0 0 1-.461-.71c.035-1.442.121-2.87.255-4.286.921.304 1.83.634 2.726.99v1.27a1.5 1.5 0 0 0-.14 2.508c-.09.38-.222.753-.397 1.11.452.213.901.434 1.346.66a6.727 6.727 0 0 0 .551-1.607 1.5 1.5 0 0 0 .14-2.67v-.645a48.549 48.549 0 0 1 3.44 1.667 2.25 2.25 0 0 0 2.12 0Z">
          </path>
          <path
            d="M4.462 19.462c.42-.419.753-.89 1-1.395.453.214.902.435 1.347.662a6.742 6.742 0 0 1-1.286 1.794.75.75 0 0 1-1.06-1.06Z">
          </path>
        </svg>
        <h3 class="text-white font-bold text-lg mb-2">BTS Systèmes Numérique option Informatique et Réseaux</h3>
        <p class="text-iris-200 text-sm">Lycée Bréquigny, Rennes | 2022-2024</p>
      </div>
    </div>
  </div>
</template>