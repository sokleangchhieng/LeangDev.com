<template>
  <section class="about">
    <div class="d-flex align-items-center mb-1">
      <h2 class="fw-bold m-0">About Me</h2>
      <div class="title-line ms-3"></div>
    </div>
    <p class="desc">{{ about.desc }}</p>

    <h3>What I do!</h3>

    <div class="grid">
      <div
        v-for="(item, index) in about.services"
        :key="index"
        :class="['card', item.color ? 'orange' : '']"
      >
        <h4>{{ item.title }}</h4>
        <p>{{ item.desc }}</p>
      </div>
    </div>
  </section>
</template>

<script>
export default {
  data() {
    return {
      about: {
        desc: " Hello! I am an IT graduate from the National Institute of Business (NIB) and currently working as a Graphic Designer. I am passionate about creating creative and visually engaging designs for digital and print media. I have experience designing social media content and marketing materials. I am detail-oriented, committed to continuous learning, and always strive to deliver high-quality designs while keeping up with the latest design trends. ",
        services: [
          {
            title: "Web Development",
            desc: "I build fast and responsive websites using modern technologies.",
            color: true,
          },
          {
            title: "Graphic Design",
            desc: "Creating clean Poster",
            color: false,
          },
          // {
          //   title: "UI/UX Designing",
          //   desc: "Designing beautiful interfaces with good user experience.",
          //   color: false,
          // },
          // {
          //   title: "Mentorship",
          //   desc: "Helping beginners grow and succeed in tech.",
          //   color: true,
          // },
        ],
      },
    };
  },
};
</script>

<style scoped>
.about {
  background: #fff;
  border-radius: 20px;
  padding: 30px;
}

.about h2 {
  margin-bottom: 10px;
}

.desc {
  color: #555;
  margin-bottom: 25px;
}

.grid {
  display: grid;
  grid-template-columns: repeat(2, 1fr);
  gap: 20px;
}

.card {
  background: #ddbbe8;
  padding: 20px;
  border-radius: 15px;
}

.card.orange {
  background: #eedef4;
}
</style>
