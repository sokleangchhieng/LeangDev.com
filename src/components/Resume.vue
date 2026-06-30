<template>
  <div class="container border-0">
    <!-- <div class="row"> -->
      <!-- CONTENT -->
      <div class="col-lg-12">
        <div>

        <div class="d-flex align-items-center mb-1">
            <h2 class="fw-bold m-0">Resume</h2>
            <div class="title-line ms-3"></div>
        </div>
          <!-- Education -->
          <div class="row mb-5">
            <div class="col-md-6">
              <h5 class="fw-bold mb-3">  <i class="iconoir-graduation-cap ms-2"></i> Education</h5>

              <div
                v-for="(edu, index) in education"
                :key="index"
                class="bg-light p-3 rounded mb-3"
              >
                <small>{{ edu.year }}</small>
                <h6 class="fw-bold mb-0">{{ edu.degree }}</h6>
                <p class="mb-0">{{ edu.school }}</p>
              </div>
            </div>

            <!-- Experience -->
            <div class="col-md-6">
              <h5 class="fw-bold mb-3"><i class="iconoir-handbag ms-2"></i> Experience</h5>

              <div
                v-for="(exp, index) in experience"
                :key="index"
                class="bg-light p-3 rounded mb-3"
              >
                <small>{{ exp.year }}</small>
                <h6 class="fw-bold mb-0">{{ exp.position }}</h6>
                <p class="mb-0">{{ exp.company }}</p>
              </div>
            </div>
          </div>

          <!-- Skills -->
          <div class="row">
            <div class="col-md-6">
              <h5 class="fw-bold mb-3"><i class="iconoir-settings"></i>  Work Skills</h5>
              <span
                v-for="(skill, index) in workSkills"
                :key="index"
                class="badge bg-light text-dark p-2 me-2 mb-2"
              >
                {{ skill }}
              </span>
            </div>

            <div class="col-md-6">
              <h5 class="fw-bold mb-3"><i class="iconoir-brain"></i>   Soft Skills</h5>
              <span
                v-for="(skill, index) in softSkills"
                :key="index"
                class="badge bg-light text-dark p-2 me-2 mb-2"
              >
                {{ skill }}
              </span>
            </div>
          </div>

        </div>
      </div>

    </div>
  <!-- </div> -->
</template>
<script setup>
import { ref } from 'vue'
const education = ref([
  {
    year: '2022 - Sep 04 2025',
    degree: 'information technology',
    school: 'National Institute of Business(NIB)'
  },
  {
    year: 'Feb 2024 - Mar 2025',
    degree: 'Studied Web Development(laravel)',
    school: 'ANT-Technology Training Center '
  }
])

const experience = ref([
  {
    year: '01-Jan-2026-Present',
    position: 'Graphic Design',
    company: 'Cambodia Scholarship Center'
  },
  {
    year: '2026-Present',
    position: 'Graphic Design',
    company: 'Makro Cambodia'
  }
])

const workSkills = ref([
  'HTML5',
  'CSS3',
  'Bootstrap',
  'JavaScript',
  'Vue.js',
  'PHP',
  'Laravel',
  'Github',
  'Photoshop',
  'illustrator',
])

const softSkills = ref([
  'Time Management',
  'Communication',
  'Flexibility',
  'Mentorship'
])
</script>
<style scoped>
    .container{
        background: #fff;
        border-radius: 20px;
        padding: 30px;
        height: 86.5vh;
    }
    i{
      color:#9024b6;
    }

</style>