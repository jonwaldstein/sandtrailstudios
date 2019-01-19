<template>
	<section class="hero-gradient bg-blue-lightest py-12">
      <div class="w-5/6 max-w-lg ml-auto mr-auto h-full">
          <div class="flex items-center justify-center text-center h-full">
              <div>
                  <h1 class="text-white text-4xl sm:text-5xl font-semibold leading-none tracking-normal mb-4 font-sans animated fadeIn">
                    Web development done right.
                  </h1>
                  <p class="text-2xl sm:text-xl text-white opacity-75 font-normal leading-tight mb-8 animated fadeIn">
                    We are a full stack web development studio specializing in <br>Wordpress, Craft CMS, Shopify, and Laravel.
                  </p>
              </div>
          </div>
      </div>
  </section>
</template>
<style>
  .animated {
    animation-duration: 1s;
    animation-fill-mode: both;
  }
  @keyframes fadeIn {
    from {
      opacity: 0;
    }

    to {
      opacity: 1;
    }
  }

  .fadeIn {
    animation-name: fadeIn;
  }
</style>