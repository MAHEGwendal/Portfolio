<template>
    <div class="bg-iris-950 p-10 mt-8">
        <h2 class="text-4xl font-bold mb-12 text-iris-100">- Contacts</h2>

        <div class="flex items-center justify-center ">
            <div class="max-w-3xl w-full text-center">
                <p class="text-xl lg:text-2xl text-gray-200 mb-8 leading-relaxed">
                    Une question, une opportunité d’alternance ou juste envie d’échanger ? N’hésitez pas à me contacter.
                    Je suis actuellement en recherche d’une alternance pour continuer à apprendre et gagner en
                    expérience, et je reste ouvert à toute discussion !
                </p>

                <a href="mailto:mahegwendal8@gmail.com">
                <button
                    class="btn text-iris-50 bg-iris-200 border-none rounded-xl p-6 mb-5 text-lg hover:bg-iris-300 hover:shadow-lg hover:shadow-iris-200/30 hover:scale-105 transition"
                    >Discutons !
                </button>
                </a>
            </div>
        </div>

        <div class="flex justify-center gap-12 pb-10">
            <a href="https://github.com/MAHEGwendal" class="hover:scale-110 transition-transform">
                <img src="/images/github_logo.webp" alt="Logo Github" class="size-15 lg:size-18" />
            </a>
            <a href="https://www.linkedin.com/in/gwendal-mahé-72ab202b7/" class="hover:scale-110 transition-transform">
                <img src="/images/LinkedIn_logo.png" alt="Logo LinkedIn" class="size-15 lg:size-18" />
            </a>
            <a href="mailto:mahegwendal8@gmail.com">
                <svg class="size-15 lg:size-18 hover:scale-110 transition-transform" data-slot="icon" fill="#6366f1"
                    viewBox="0 0 24 24" xmlns="http://www.w3.org/2000/svg" aria-hidden="true">
                    <path
                        d="M1.5 8.67v8.58a3 3 0 0 0 3 3h15a3 3 0 0 0 3-3V8.67l-8.928 5.493a3 3 0 0 1-3.144 0L1.5 8.67Z">
                    </path>
                    <path
                        d="M22.5 6.908V6.75a3 3 0 0 0-3-3h-15a3 3 0 0 0-3 3v.158l9.714 5.978a1.5 1.5 0 0 0 1.572 0L22.5 6.908Z">
                    </path>
                </svg>
            </a>
        </div>
    </div>
</template>