<template>
  <v-container fluid class="pa-6 testimonials-section">
    <h2 class="text-center mb-8">What our clients say</h2>

    <!-- Row 1: moves RIGHT -->
    <div class="marquee" :style="{ '--duration': duration + 's' }">
      <div class="track track--right" aria-hidden="true">
        <v-card
          v-for="(t, i) in row1Loop"
          :key="'r1-' + i"
          class="testimonial-card"
          elevation="2"
        >
          <v-card-text>
            <div class="quote-mark">“</div>
            <div class="text-body-2 mb-4">{{ t.text }}</div>

            <div class="d-flex align-center gap-3">
              <v-avatar size="32" color="grey-lighten-3">
                <span class="text-caption font-weight-bold">
                  {{ initials(t.name) }}
                </span>
              </v-avatar>

              <div>
                <div class="text-subtitle-2 font-weight-medium">{{ t.name }}</div>
                <div class="text-caption text--secondary">{{ t.meta }}</div>
              </div>
            </div>
          </v-card-text>
        </v-card>
      </div>
    </div>

    <!-- Row 2: moves LEFT -->
    <div class="marquee mt-6" :style="{ '--duration': duration + 's' }">
      <div class="track track--left" aria-hidden="true">
        <v-card
          v-for="(t, i) in row2Loop"
          :key="'r2-' + i"
          class="testimonial-card"
          elevation="2"
        >
          <v-card-text>
            <div class="quote-mark">“</div>
            <div class="text-body-2 mb-4">{{ t.text }}</div>

            <div class="d-flex align-center gap-3">
              <v-avatar size="32" color="grey-lighten-3">
                <span class="text-caption font-weight-bold">
                  {{ initials(t.name) }}
                </span>
              </v-avatar>

              <div>
                <div class="text-subtitle-2 font-weight-medium">{{ t.name }}</div>
                <div class="text-caption text--secondary">{{ t.meta }}</div>
              </div>
            </div>
          </v-card-text>
        </v-card>
      </div>
    </div>
  </v-container>
</template>

<script>
export default {
  name: "Testimonials",
  data() {
    return {
      duration: 22, // lower = faster, higher = slower
      testimonials: [
        { name: "Alice R.", text: "Great service — on time and professional.", meta: "Gate installation, 2025" },
        { name: "Ben K.", text: "High quality work and friendly team.", meta: "Custom railing, 2024" },
        { name: "Carla M.", text: "Fast turnaround and excellent finish.", meta: "Driveway gate, 2025" },
        { name: "Daniel P.", text: "Would recommend — superb attention to detail.", meta: "Garden gate, 2023" },
        { name: "Ethan S.", text: "Clean workmanship and very responsive.", meta: "Metal grilles, 2024" },
        { name: "Farah N.", text: "Exactly what we wanted. Strong and sleek.", meta: "Main gate, 2025" }
      ]
    };
  },
  computed: {
    // split into two rows
    row1() {
      return this.testimonials.filter((_, i) => i % 2 === 0);
    },
    row2() {
      return this.testimonials.filter((_, i) => i % 2 === 1);
    },

    // duplicate to create seamless loop
    row1Loop() {
      return [...this.row1, ...this.row1, ...this.row1];
    },
    row2Loop() {
      return [...this.row2, ...this.row2, ...this.row2];
    }
  },
  methods: {
    initials(name) {
      return name
        .replace(".", "")
        .split(" ")
        .filter(Boolean)
        .slice(0, 2)
        .map((w) => w[0].toUpperCase())
        .join("");
    }
  }
};
</script>

<style scoped>
.testimonials-section {
  overflow: hidden; /* hides the moving overflow cleanly */
}

/* container for each moving row */
.marquee {
  position: relative;
  overflow: hidden;
  width: 100%;
  padding: 4px 0;
}

/* track that moves */
.track {
  display: flex;
  gap: 16px;
  width: max-content;
  will-change: transform;
}

/* pause animation on hover (nice UX) */
.marquee:hover .track {
  animation-play-state: paused;
}

/* RIGHT direction: starts off-screen left -> moves to the right */
.track--right {
  transform: translateX(-40%);
  animation: moveRight var(--duration, 22s) linear infinite;
}

/* LEFT direction: starts off-screen -> moves left */
.track--left {
  transform: translateX(0%);
  animation: moveLeft var(--duration, 22s) linear infinite;
}

@keyframes moveRight {
  from {
    transform: translateX(-40%);
  }
  to {
    transform: translateX(0%);
  }
}

@keyframes moveLeft {
  from {
    transform: translateX(0%);
  }
  to {
    transform: translateX(-40%);
  }
}

/* card styling */
.testimonial-card {
  width: 340px;
  border-radius: 16px;
  flex: 0 0 auto;
  transition: transform 0.2s ease, box-shadow 0.2s ease;
}

.testimonial-card:hover {
  transform: translateY(-4px);
}

/* quote mark */
.quote-mark {
  font-size: 28px;
  line-height: 1;
  opacity: 0.25;
  margin-bottom: 8px;
}

/* accessibility: respect reduced motion */
@media (prefers-reduced-motion: reduce) {
  .track--right,
  .track--left {
    animation: none !important;
    transform: none !important;
  }
}
</style>
