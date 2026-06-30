<script setup lang="ts">
import { ref, computed } from "vue";

// Portfolio Projects
const projects = ref([
  {
    title: "Even",
    type: "Design",
    category: "Design",
    image: "/assets/images/Even24-25-3.jpg",
    link: "/assets/images/Even24-25-3.jpg",
  },
   {
    title: "chabhuoy",
    type: "Design",
    category: "Design",
    image: "/assets/images/chabhuoy.jpg",
    link: "/assets/images/chabhuoy.jpg",
  },
  {
    title: "TOST REAN",
    type: "Web Development",
    category: "Bootstrap",
    image: "/assets/images/Bootstrap.png",
    link: "http://antstudents.com/WebScholarshipS2/Group-8/ProjectCSS_TosRean/index.html",
  },
  {
    title: "Portfolio Website",
    type: "Web Development",
    category: "JavaScript",
    image: "/assets/images/javascript.png",
    link: "#",
  },
  {
    title: "Charity System",
    type: "Web Development",
    category: "PHP/Laravel",
    image: "/assets/images/php.png",
    link: "#",
  },

  {
    title: "New Arrivals",
    type: "Design",
    category: "Design",
    image: "/assets/images/New_Arrivals_Header.jpg",
    link: "/assets/images/New_Arrivals_Header.jpg",
  },
  {
    title: "WeeklyFF",
    type: "Design",
    category: "Design",
    image: "/assets/images/WeeklyFF.png",
    link: "/assets/images/WeeklyFF.png",
  },

  {
    title: "header website",
    type: "Design",
    category: "Design",
    image: "/assets/images/laundry.jpg",
    link: "/assets/images/laundry.jpg",
  },
  {
    title: "Poster",
    type: "Design",
    category: "Design",
    image: "/assets/images/BD-01.jpg",
    link: "/assets/images/BD-01.jpg",
  },
   {
    title: "TOST REAN",
    type: "Web Development",
    category: "HTML/CSS",
    image: "/assets/images/html_css.png",
    link: "http://antstudents.com/WebScholarship/Group-18/ProjectHTML/index.html",
  },
  {
    title: "Poster",
    type: "Design",
    category: "Design",
    image: "/assets/images/Royal .jpg",
    link: "/assets/images/Royal .jpg",
  },
  {
    title: "Logo",
    type: "Design",
    category: "Design",
    image: "/assets/images/logo.png",
    link: "/assets/images/logo.png",
  },
  {
    title: "Logo",
    type: "Design",
    category: "Design",
    image: "/assets/images/Logo-2.png",
    link: "/assets/images/Logo-2.png",
  },
  {
    title: "Poster",
    type: "Design",
    category: "Design",
    image: "/assets/images/Ausstralia_1.jpg",
    link: "/assets/images/Ausstralia_1.jpg",
  },
  {
    title: "Poster",
    type: "Design",
    category: "Design",
    image: "/assets/images/Australia_Scholarship-1.jpg",
    link: "/assets/images/Australia_Scholarship-1.jpg",
  },
  {
    title: "Poster",
    type: "Design",
    category: "Design",
    image: "/assets/images/Australiaaa-1.jpg",
    link: "/assets/images/Australiaaa-1.jpg",
  },
  {
    title: "Poster",
    type: "Design",
    category: "Design",
    image: "/assets/images/japan_scholarship-1.jpg",
    link: "/assets/images/japan_scholarship-1.jpg",
  },
  {
    title: "Poster",
    type: "Design",
    category: "Design",
    image: "/assets/images/korea_scholarship-1.jpg",
    link: "/assets/images/korea_scholarship-1.jpg",
  },
  {
    title: "Poster",
    type: "Design",
    category: "Design",
    image: "/assets/images/Romania_scholarship.jpg",
    link: "/assets/images/Romania_scholarship.jpg",
  },
  {
    title: "Poster",
    type: "Design",
    category: "Design",
    image: "/assets/images/scholarship_turkey03.jpg",
    link: "/assets/images/scholarship_turkey03.jpg",
  },
   {
    title: "Poster",
    type: "Design",
    category: "Design",
    image: "/assets/images/singapore.jpg",
    link: "/assets/images/singapore.jpg",
  },
   {
    title: "Poster",
    type: "Design",
    category: "Design",
    image: "/assets/images/UK-1.jpg",
    link: "/assets/images/UK-1.jpg",
  },
  {
    title: "Even",
    type: "Design",
    category: "Design",
    image: "/assets/images/Even-24-25-1.jpg",
    link: "/assets/images/Even-24-25-1.jpg",
  },
   {
    title: "Even",
    type: "Design",
    category: "Design",
    image: "/assets/images/Even24-25-2.jpg",
    link: "/assets/images/Even24-25-2.jpg",
  },
   {
    title: "Even",
    type: "Design",
    category: "Design",
    image: "/assets/images/Even24-25-3.jpg",
    link: "/assets/images/Even24-25-3.jpg",
  },
  {
    title: "Poster",
    type: "Design",
    category: "Design",
    image: "/assets/images/couse_scholarship-1.jpg",
    link: "/assets/images/couse_scholarship-1.jpg",
  },
  {
    title: "Poster",
    type: "Design",
    category: "Design",
    image: "/assets/images/china_scholarship-1.jpg",
    link: "/assets/images/china_scholarship-1.jpg",
  },
  
  
  
  
  
]);

// Categories
const categories = ["All", "Web Development", "Design"];

const selectedCategory = ref("All");

// Filter
const filteredProjects = computed(() => {
  if (selectedCategory.value === "All") {
    return projects.value;
  }

  return projects.value.filter(
    (item) => item.type === selectedCategory.value
  );
});
</script>

<template>
  <div class="portfolio-card shadow-sm">

    <div class="d-flex align-items-center mb-4">
      <h2 class="fw-bold mb-0">Portfolio</h2>
      <div class="title-line ms-3"></div>
    </div>

    <!-- Filter -->

    <ul class="nav filter-nav mb-4">

      <li
        v-for="cat in categories"
        :key="cat"
        class="nav-item"
      >

        <button
          class="nav-link border-0 bg-transparent"
          :class="{ active: selectedCategory === cat }"
          @click="selectedCategory = cat"
        >
          {{ cat }}
        </button>

      </li>

    </ul>

    <!-- Projects -->

    <div class="row g-4">

      <div
        v-for="(project,index) in filteredProjects"
        :key="index"
        class="col-lg-6 col-md-6"
      >

        <a
          :href="project.link"
          target="_blank"
          class="text-decoration-none"
        >

          <div class="project-card">

            <div class="image-box">

              <img
                :src="project.image"
                :alt="project.title"
              >

              <div class="overlay">
                <span>View Project</span>
              </div>

            </div>

            <div class="content">

              <small>{{ project.category }}</small>

              <h5>{{ project.title }}</h5>

            </div>

          </div>

        </a>

      </div>

    </div>

  </div>
</template>

<style scoped>

.portfolio-card{
    background:#fff;
    padding:30px;
    border-radius:20px;
}

/* Heading */

.title-line{
    width:120px;
    height:2px;
    background:#ff6b35;
}

/* Filter */

.filter-nav{
    gap:10px;
}

.filter-nav .nav-link{
    color:#666;
    font-weight:500;
    transition:.3s;
}

.filter-nav .nav-link:hover{
    color:#ff6b35;
}

.filter-nav .active{
    color:#ff6b35;
    font-weight:700;
}

/* Card */

.project-card{
    border-radius:18px;
    overflow:hidden;
    background:#fff;
    box-shadow:0 10px 25px rgba(0,0,0,.08);
    transition:.35s;
}

.project-card:hover{
    transform:translateY(-8px);
}

/* Image */

.image-box{
    position:relative;
    overflow:hidden;
}

.image-box img{
    width:100%;
    height:240px;
    object-fit:cover;
    transition:.5s;
}

.project-card:hover img{
    transform:scale(1.08);
}

/* Overlay */

.overlay{
    position:absolute;
    inset:0;
    background:rgba(255,107,53,.82);

    display:flex;
    justify-content:center;
    align-items:center;

    opacity:0;
    transition:.4s;
}

.project-card:hover .overlay{
    opacity:1;
}

.overlay span{
    color:#fff;
    border:2px solid white;
    padding:12px 28px;
    border-radius:30px;
    font-weight:600;
}

/* Content */

.content{
    padding:20px;
}

.content small{
    color:#ff6b35;
    font-weight:600;
}

.content h5{
    margin-top:8px;
    color:#222;
    font-weight:700;
}

/* Responsive */

@media(max-width:768px){

.image-box img{
    height:200px;
}

.portfolio-card{
    padding:20px;
}

}

</style>