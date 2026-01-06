<template>
    <v-container fluid class ="pa-0" style="background-color: #2F3E2E;">
        <v-timeline align-top>
            <v-timeline-item
                v-for="(step, i) in steps"
                :key="i"
                dot-color="transparent"
                size="24"
                >
                <template #icon>
                    <div class="timeline-dot"></div>
                </template>

                <v-card elevation="2" class="pa-4">
                    <h3 class="mb-2">{{ step.title }}</h3>
                    <p class="mb-0">{{ step.desc }}</p>
                </v-card>
                </v-timeline-item>
        </v-timeline>
    </v-container>
</template>

<script>
export default {
  name: 'Process',
  data() {
    return {
      steps: [
        {
          title: 'Consultation',
          desc: 'We meet at your property to discuss your vision, take precise measurements, and provide a transparent quote.'
        },
        {
          title: 'Fabrication',
          desc: 'Our expert welders hand-craft your gate in our local workshop using high-grade steel and traditional techniques.'
        },
        {
          title: 'Installation',
          desc: 'We professionally fit your gate, ensuring smooth operation and a perfect finish that lasts for years.'
        }
      ]
    }
  }
}
</script>

<style scoped>
/* tweak spacing / card width on large screens */
.v-timeline {
  max-width: 900px;
  margin: 0 auto;
}

/* Custom dot */
.timeline-dot {
  width: 14px;
  height: 14px;
  border-radius: 50%;
  border: 2px solid rgba(255, 255, 255, 0.7);
  background-color: transparent;
}

/* Optional: make the vertical line subtle */
:deep(.v-timeline-divider__line) {
  background-color: rgba(255, 255, 255, 0.25);
}
</style>