<template>
  <div class="tokyo_tm_contact">
    <div class="tokyo_tm_title">
      <div class="title_flex">
        <div class="left">
          <span>Contact</span>
          <h3>Get in Touch</h3>
        </div>
      </div>
    </div>
    <!-- End Title -->

    <div class="map_wrap">
      <iframe
        id="gmap_canvas"
        src="https://www.google.com/maps/embed/v1/place?q=place_id:ChIJ7THRiJQ9UocRyjFNSKC3U1s&key=AIzaSyCO5qVeFTpsHpFITnaF2yNnmDpIr8G69oo"
        marginheight="0"
        marginwidth="0"
      ></iframe>
    </div>
    <!-- End Google Map -->

    <div class="fields">
      <ValidationObserver v-slot="{ handleSubmit }">
        <form class="contact_form" @submit.prevent="handleSubmit(onSubmit)">
          <div class="first">
            <ul>
              <ValidationProvider
                name="name"
                rules="required"
                v-slot="{ errors }"
              >
                <li>
                  <input
                    v-model="formData.name"
                    type="text"
                    placeholder="Name"
                    autocomplete="off"
                  />
                  <span class="inpur-error">{{ errors[0] }}</span>
                </li>
              </ValidationProvider>

              <ValidationProvider
                name="email"
                rules="required|email"
                v-slot="{ errors }"
              >
                <li>
                  <input
                    type="text"
                    rules="required|email"
                    v-model="formData.email"
                    placeholder="email"
                  />
                  <span class="inpur-error">{{ errors[0] }}</span>
                </li>
              </ValidationProvider>
              <ValidationProvider
                name="message"
                rules="required"
                v-slot="{ errors }"
              >
                <li>
                  <textarea
                    v-model="formData.message"
                    placeholder="Message"
                  ></textarea>
                  <span class="inpur-error">{{ errors[0] }}</span>
                </li>
              </ValidationProvider>
            </ul>
          </div>
          <div class="tokyo_tm_button">
            <button type="submit" class="ib-button">Send Message</button>
          </div>
        </form>
      </ValidationObserver>
    </div>
    <!-- END FIELDS -->
  </div>
</template>

<script>
  import { ValidationObserver } from "vee-validate";
  import { ValidationProvider } from "vee-validate/dist/vee-validate.full.esm";
  export default {
    components: {
      ValidationObserver,
      ValidationProvider
    },
    data() {
      return {
        formData: {
          name: "",
          email: "",
          message: "",
        },
      };
    },
    methods: {
      onSubmit() {
        console.log(this.formData);
        // console.log('key: ', process.env.GOOGLE_API_KEY);
      },
    },
  };
</script>
