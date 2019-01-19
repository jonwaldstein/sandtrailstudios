<template>
  <div class="font-sans text-black h-full">        

        <Banner />
        <section class="bg-white py-8">
            <div class="w-5/6 max-w-2xl ml-auto mr-auto mt-8 mb-8">
                <div class="flex flex-wrap -mx-6 -my-6 text-center">
                    <div class="w-full md:w-1/2 px-6 py-6">
                      <div class="max-w-xs mx-auto">
                        <div class="mb-8">
                            <span class="align-middle text-blue-dark fa-4x fab fa-wordpress-simple"></span>
                          </div>
                          <h3 class="text-3xl sm:text-4xl font-semibold tracking-tight leading-none mb-3">Wordpress</h3>
                          <p class="text-lg sm:text-xl leading-normal text-grey-darker mb-8">Custom themes, plugins, and solutions.</p>
                      </div>
                    </div>
                    <div class="w-full md:w-1/2 px-6 py-6">
                      <div class="max-w-xs mx-auto">
                        <div class="mb-8">
                          <img class="align-middle w-48" src="~/assets/images/craft-logo.svg" alt="">
                        </div>
                        <h3 class="text-3xl sm:text-4xl font-semibold tracking-tight leading-none mb-3">Craft CMS</h3>
                        <p class="text-lg sm:text-xl leading-normal text-grey-darker mb-8">For larger websites with complex content types and relationships.</p>
                      </div>
                    </div>
                    <div class="w-full md:w-1/2 px-6 py-6">
                      <div class="max-w-xs mx-auto">
                        <div class="mb-8">
                          <span class="align-middle text-red fa-4x fab fa-laravel"></span>
                        </div>
                        <h3 class="text-3xl sm:text-4xl font-semibold tracking-tight leading-none mb-3">Laravel</h3>
                        <p class="text-lg sm:text-xl leading-normal text-grey-darker mb-8">Web appliciation development.</p>
                      </div>
                    </div>
                    <div class="w-full md:w-1/2 px-6 py-6">
                      <div class="max-w-xs mx-auto">
                          <div class="mb-8">
                            <img class="align-middle w-16" src="~/assets/images/shopify-logo.svg" alt="">
                          </div>
                          <h3 class="text-3xl sm:text-4xl font-semibold tracking-tight leading-none mb-3">Shopify</h3>
                          <p class="text-lg sm:text-xl leading-normal text-grey-darker mb-8">Get your e-commerce store up and running.</p>
                      </div>
                    </div>
                </div>
            </div>
        </section>

        <section class=" py-8">
            <div class="w-5/6 max-w-2xl ml-auto mr-auto mt-8">
                <div class="flex flex-wrap -mx-6 -my-6">
                    <div class="w-full lg:w-1/3 px-6 py-6">
                        <a class="no-underline" href="#">
                            <div class="bg-white rounded shadow-lg overflow-hidden p-8">
                                <h5 class="text-2xl text-blue-dark mb-4">Web & UX Design</h5>
                                <p class="text-lg text-blue-dark leading-tight">We know a thing or two about design trends and what helps convert.</p>
                            </div>
                        </a>
                    </div>
                    <div class="w-full lg:w-1/3 px-6 py-6">
                        <a class="no-underline" href="#">
                            <div class="bg-teal-dark rounded shadow-lg overflow-hidden p-8">
                                <h5 class="text-2xl text-white mb-4">Web & Application Development</h5>
                                <p class="text-lg text-white leading-tight">We like to build quality things for cool people.</p>
                            </div>
                        </a>
                    </div>
                    <div class="w-full lg:w-1/3 px-6 py-6">
                        <a class="no-underline" href="#">
                            <div class="bg-white rounded shadow-lg overflow-hidden p-8">
                                <h5 class="text-2xl text-blue-dark mb-4">Digital Consulting</h5>
                                <p class="text-lg text-blue-dark leading-tight">Don't go at it alone.  Let us help you navigate this world of digital madness. </p>
                            </div>
                        </a>
                    </div>
                </div>
            </div>
        </section>

        <section class="bg-grey-lightest py-8">
            <div class="w-5/6 max-w-xl ml-auto mr-auto my-8">
                <div class="flex md:items-center flex-col md:flex-row md:justify-between">
                    <div class="mb-8 md:mb-0 md:pr-4">
                        <h3 class="text-4xl font-normal leading-none mb-3">Ready to talk?</h3>
                        <h4 class="text-2xl text-grey-dark font-normal leading-tight">
                        Don't be shy, we don't charge for a conversation.
                        </h4>
                    </div>
                    <div class="md:pl-4">
                        <div class="flex items-center">
                            <button class="bg-teal hover:bg-teal-dark text-xl leading-none text-white font-semibold h-10 px-6 rounded-full whitespace-no-wrap mr-2">
                                Contact Us
                            </button>
                        </div>
                    </div>
                </div>
            </div>
        </section>

        <Footer />
    </div>
</template>

<script>
import Logo from '~/components/Logo.vue'
import Header from '~/components/Header.vue'
import Banner from '~/components/Home/Banner.vue'
import Footer from '~/components/Footer.vue'

export default {
  components: {
    Logo,
    Header,
    Banner,
    Footer
  }
}
</script>
