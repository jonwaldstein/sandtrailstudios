<template>
  <section class="container mx-auto py-5 mb-5 px-2">
    <div class="w-full mb-8 mx-auto text-center">
        <h3 class="text-2xl font-normal leading-none mb-3">Ready to talk?</h3>
        <p class="text-lg text-grey-dark font-normal leading-tight">
        Don't be shy, we don't charge for a conversation.
        </p>
    </div>
    <form class="w-full max-w-md mx-auto" action="https://formspree.io/jpwaldstein@gmail.com" method="POST">
      <div class="flex flex-wrap -mx-3 mb-6">
        <div class="w-full md:w-1/2 px-3 mb-6 md:mb-0">
          <label class="block uppercase tracking-wide text-grey-darker text-xs font-bold mb-2" for="grid-first-name">
            Name
          </label>
          <input class="appearance-none block w-full bg-grey-lighter text-grey-darker border rounded py-3 px-4 leading-tight focus:outline-none focus:bg-white" :class="{ 'border-red': this.nameError }" type="text" placeholder="Jane Doe" name="Name" id="name" required>
          {{name}}
          <p v-if="this.nameError" class="text-red text-xs italic">{{this.nameError}}</p>
        </div>
        <div class="w-full md:w-1/2 px-3">
          <label class="block uppercase tracking-wide text-grey-darker text-xs font-bold mb-2" for="grid-last-name">
            Email
          </label>
          <input class="appearance-none block w-full bg-grey-lighter text-grey-darker border border-grey-lighter rounded py-3 px-4 leading-tight focus:outline-none focus:bg-white focus:border-grey" type="email" placeholder="example@gmail.com" name="email" id="email" required :class="{ 'border-red': this.emailError }">
          <p v-if="this.emailError" class="text-red text-xs italic">{{this.emailError}}</p>
        </div>
      </div>
        <div class="w-full mb-4">
            <label class="block uppercase tracking-wide text-grey-darker text-xs font-bold mb-2" for="grid-message">
              Message
            </label>
            <textarea rows="4" cols="50" id="message" class="appearance-none block w-full bg-grey-lighter text-grey-darker border border-grey-lighter rounded py-3 px-4 leading-tight focus:outline-none focus:bg-white focus:border-grey" name="Message" required :class="{ 'border-red': this.messageError }"></textarea>
            <p v-if="this.messageError" class="text-red text-xs italic">{{this.messageError}}</p>
        </div>
        <div class="w-full">
          <button type="submit" class="bg-teal hover:bg-teal-dark text-xl leading-none text-white font-semibold h-10 px-6 rounded-full whitespace-no-wrap mr-2">Contact Us</button>
        </div>
    </form>
</section>
</template>
<script>
  export default{
    data(){
      return{
        errors: [],
        name: '',
        nameError: '',
        email: '',
        emailError: '',
        message: '',
        messageError: '',
      }
    },
    methods:{
      checkForm: function (e) {

        this.errors = [];

        if (!this.name) {
          this.errors.push("Name required.");
          this.nameError = 'Name required.';
        }
         if (!this.email) {
          this.errors.push("Email required.");
          this.emailError = 'Email required.';
        } else if (!this.validEmail(this.email)) {
          this.errors.push("Email required.");
          this.emailError = 'Valid email required.';
        }
        if (!this.message) {
          this.errors.push("A message required.");
          this.messageError = 'A message required.';
        }
        if (!this.errors.length) {
          return true;
        }

        e.preventDefault();
      },
      validEmail: function (email) {
        var re = /^(([^<>()\[\]\\.,;:\s@"]+(\.[^<>()\[\]\\.,;:\s@"]+)*)|(".+"))@((\[[0-9]{1,3}\.[0-9]{1,3}\.[0-9]{1,3}\.[0-9]{1,3}\])|(([a-zA-Z\-0-9]+\.)+[a-zA-Z]{2,}))$/;
        return re.test(email);
      }
    }
  }
</script>