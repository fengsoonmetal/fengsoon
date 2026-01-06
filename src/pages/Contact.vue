<template>
  <v-container class="py-16">
    <!-- Page header -->
    <div class="text-center mb-12">
      <h1 class="text-h4 font-weight-bold mb-4">Contact Us</h1>
      <p class="text-body-1 text-medium-emphasis mx-auto" style="max-width: 720px;">
        Get in touch with us for enquiries, repairs, or a consultation. We will respond as soon as possible.
      </p>
    </div>

    <v-row justify="center">
      <!-- Contact details -->
      <v-col cols="12" md="5">
        <v-card elevation="2" class="pa-6 h-100">
          <h2 class="text-h6 font-weight-bold mb-4">Our Contact Information</h2>

          <div class="mb-4">
            <div class="text-subtitle-2 font-weight-medium">Phone</div>
            <div class="text-body-1">+65 9123 4567</div>
          </div>

          <div class="mb-4">
            <div class="text-subtitle-2 font-weight-medium">Email</div>
            <div class="text-body-1">fengsoon@hotmail.com</div>
          </div>

          <div class="mb-4">
            <div class="text-subtitle-2 font-weight-medium">Operating Hours</div>
            <div class="text-body-1">
              Monday – Saturday<br />
              9:00 AM – 6:00 PM
            </div>
          </div>

          <div>
            <div class="text-subtitle-2 font-weight-medium">Service Areas</div>
            <div class="text-body-1">
              Residential & Commercial Projects
            </div>
          </div>
        </v-card>
      </v-col>

      <!-- Contact form -->
      <v-col cols="12" md="7">
        <v-card elevation="2" class="pa-6 h-100">
          <h2 class="text-h6 font-weight-bold mb-4">Send Us a Message</h2>

          <v-form>
            <v-text-field
              label="Full Name"
              variant="outlined"
              class="mb-4"
              required
            />

            <v-text-field
              label="Contact Number"
              variant="outlined"
              class="mb-4"
              required
            />

            <v-text-field
              label="Email Address"
              variant="outlined"
              class="mb-4"
              required
            />

            <v-textarea
              label="Message"
              variant="outlined"
              rows="4"
              class="mb-6"
              placeholder="Tell us more about your enquiry..."
            />

            <v-btn color="primary" size="large">
              Submit Enquiry
            </v-btn>
          </v-form>
        </v-card>
      </v-col>
    </v-row>
  </v-container>
</template>
