<template>
  <v-container class="py-16">
    <!-- Page header -->
    <div class="about-hero">
        <v-container class="py-16">
            <div class="text-center mb-12">
            <h1 class="text-h4 font-weight-bold mb-4 text-white">
                About Us
            </h1>

            <p class="text-body-1 text-white text-opacity-80 mx-auto"
                style="max-width: 720px;">
                Trusted metal works specialists delivering reliable craftsmanship for over a decade.
            </p>
            </div>

            <v-row justify="center">
            <v-col cols="12" md="8">
                <div class="text-body-1 text-white text-opacity-90" style="line-height: 1.8;">
                <p>
                    Feng Soon is a locally established metal works specialist, serving residential and
                    commercial clients with dependable and practical solutions. Established in 2008,
                    we have built our reputation on quality workmanship, honest service, and attention
                    to detail.
                </p>

                <p>
                    With decades of combined industry experience, our team specialises in metal gate
                    installations, roller replacements, and hinge replacements. We focus on durable
                    materials, precise fitting, and long-lasting performance.
                </p>

                <p>
                    Whether it is a new installation or repair and replacement work, we approach every
                    project with the same level of care and professionalism.
                </p>
                </div>
            </v-col>
            </v-row>
        </v-container>
        </div>


    <!-- Highlights -->
    <v-row class="mt-12" justify="center" align="stretch">
        <v-col cols="12" sm="6" md="4">
            <v-card elevation="2" class="pa-6 text-center h-100">
            <div class="text-h5 font-weight-bold mb-2">Established</div>
            <div class="text-h4 font-weight-bold">2008</div>
            </v-card>
        </v-col>

        <v-col cols="12" sm="6" md="4">
            <v-card elevation="2" class="pa-6 text-center h-100">
            <div class="text-h5 font-weight-bold mb-2">Experience</div>
            <div class="text-h4 font-weight-bold">Decades</div>
            </v-card>
        </v-col>

        <v-col cols="12" sm="6" md="4">
            <v-card elevation="2" class="pa-6 text-center h-100">
            <div class="text-h5 font-weight-bold mb-2">Specialisation</div>
            <div class="text-body-1">
                Metal Gates<br />
                Roller Replacement<br />
                Hinge Replacement
            </div>
            </v-card>
        </v-col>
        </v-row>
  </v-container>
</template>

<style scoped>
.about-hero {
  position: relative;
  background-image: url('@/assets/metal_gate.jpeg');
  background-size: cover;
  background-position: center;
}

.about-hero::before {
  content: '';
  position: absolute;
  inset: 0;
  background: rgba(0, 0, 0, 0.55); /* controls darkness */
}

.about-hero > * {
  position: relative;
  z-index: 1;
}
</style>
