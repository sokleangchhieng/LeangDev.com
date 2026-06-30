<template>
  <div class="mt-3">
    <h5>Work Skills</h5>
    <div class="d-flex flex-wrap gap-2">
      <span v-for="skill in workSkills" :key="skill" class="badge bg-light text-dark">{{ skill }}</span>
    </div>

    <h5 class="mt-3">Soft Skills</h5>
    <div class="d-flex flex-wrap gap-2">
      <span v-for="skill in softSkills" :key="skill" class="badge bg-light text-dark">{{ skill }}</span>
    </div>
  </div>
</template>

<script setup lang="ts">
const workSkills = ['NEXT.js', 'React.js', 'HTML5', 'CSS3', 'Tailwind CSS', 'Figma', 'JavaScript', 'MongoDB', 'SQL', 'Angular', 'Android', 'Git']
const softSkills = ['Time Management', 'Mentorship', 'Impeccable Communication', 'Flexibility', 'Research', 'Writing']
</script>
