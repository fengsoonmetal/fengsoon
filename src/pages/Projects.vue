<template>
  <v-container class="py-16">
    <!-- Page header -->
    <div class="text-center mb-10">
      <h1 class="text-h4 font-weight-bold mb-3">Past Projects</h1>
      <p class="text-body-1 text-medium-emphasis">
        A selection of our completed works, showcasing our craftsmanship and attention to detail.
      </p>
    </div>

    <!-- Projects grid -->
    <v-row>
      <v-col
        v-for="(project, index) in projects"
        :key="index"
        cols="12"
        sm="6"
        md="4"
      >
        <v-card elevation="2" class="project-card">
          <!-- Placeholder image -->
          <v-img
            height="180"
            src="https://via.placeholder.com/600x400?text=Project+Image"
            cover
          />

          <v-card-text>
            <div class="text-subtitle-1 font-weight-medium mb-1">
              {{ project.title }}
            </div>

            <div class="text-caption text-medium-emphasis mb-2">
              {{ project.category }} • {{ project.year }}
            </div>

            <div class="text-body-2">
              {{ project.description }}
            </div>
          </v-card-text>
        </v-card>
      </v-col>
    </v-row>
  </v-container>
</template>

<script setup>
const projects = [
  {
    title: 'Residential Sliding Gate',
    category: 'Gate Installation',
    year: '2025',
    description: 'Custom-designed sliding gate with durable steel framing and smooth motorised operation.'
  },
  {
    title: 'Balcony Metal Railing',
    category: 'Metal Railing',
    year: '2024',
    description: 'Minimalist railing design providing both safety and aesthetic appeal for a private residence.'
  },
  {
    title: 'Driveway Swing Gate',
    category: 'Gate Installation',
    year: '2024',
    description: 'Heavy-duty swing gate engineered for long-term outdoor durability and reliability.'
  },
  {
    title: 'Garden Fence & Gate',
    category: 'Fencing',
    year: '2023',
    description: 'Custom fence and gate solution designed to complement the surrounding landscape.'
  },
  {
    title: 'Industrial Security Gate',
    category: 'Commercial Project',
    year: '2023',
    description: 'Robust security gate installation for industrial premises with reinforced steel components.'
  },
  {
    title: 'Staircase Handrail',
    category: 'Metal Works',
    year: '2022',
    description: 'Precision-fabricated handrail with clean welds and smooth finishing.'
  }
]
</script>

<style scoped>
.project-card {
  transition: transform 0.2s ease, box-shadow 0.2s ease;
}

.project-card:hover {
  transform: translateY(-4px);
}
</style>
