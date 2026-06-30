<template>
  <aside class="sidebar">
    <img :src="profile.avatar" :alt="profile.name" class="avatar" />

    <h2 class="name">{{ profile.name }}</h2>
    <p class="title">{{ profile.title }}</p>

    <div class="socials">
      <a
        v-for="social in profile.socials"
        :key="social.name"
        :href="social.link"
        target="_blank"
        rel="noopener noreferrer"
      >
        <i :class="social.icon"></i>
      </a>
    </div>

    <div class="info">
      <p><strong><i class="iconoir-smartphone-device"></i> Phone:<br/></strong>{{ profile.phone }}</p>
      <p><strong><i class="iconoir-mail-open"></i> Email:</strong> {{ profile.email }}</p>
      <p><strong><i class="iconoir-map-pin"></i> Location:<br /></strong> {{ profile.location }}</p>
    </div>

    <button class="btn" @click="downloadResume">
     <i class="iconoir-download"></i> Download Resume
    </button>
  </aside>
</template>

<script>
export default {
  data() {
    return {
      profile: {
        name: "Chhieang SokLeang",
        title: "Designer",
        avatar: "/leang.JPG",
        phone: "+855 93374939",
        email: "sokleangchieang123@gmail.com",
        location: "Sangkat Boeng Tumpoun2, Meanchey District, Phnom Penh",
        socials: [
          {
            name: "Facebook",
            link: "https://www.facebook.com/share/17WcFGmpnm/?mibextid=wwXIfr",
            icon: "iconoir-facebook-tag",
          },
          {
            name: "Linkedin",
            link: "https://www.linkedin.com/in/chhieang-sok-leang",
            icon: "iconoir-linkedin",
          },
          {
            name: "GitHub",
            link: "https://github.com/sokleangchhieng",
            icon: "iconoir-github-circle",
          },
          {
            name: "Telegram",
            link: "https://t.me/kesorr4444",
            icon: "iconoir-telegram-circle",
          },
        ],
      },
    };
  },
  methods: {
    downloadResume() {
      window.open("/public/CHHIEANGSOKLEANG.pdf", "_blank");
    },
  },
};
</script>

<style scoped>
.sidebar {
  width: 280px;
  background: #fff;
  border-radius: 20px;
  padding: 30px;
  text-align: center;
}

.avatar {
  width: 120px;
  height: 120px;
  border-radius: 20px;
  object-fit: cover;
  margin-bottom: 15px;
}

.name {
  font-size: 20px;
  font-weight: bold;
}

.title {
  color: gray;
  margin-bottom: 15px;
}

.socials {
  display: flex;
  justify-content:space-around;
  gap: 10px;
  margin-bottom: 15px;
}

.socials a {
  background: #f2f2f2;
  padding: 10px;
  border-radius: 8px;
  display: flex;
  align-items: center;
  justify-content: center;
  font-size: 22px;
  color:#9024b6;
  transition: all 0.2s ease;
}

.socials a:hover {
  background: #9024b6;
  color: #fff;
  transform: scale(1.15);
}

.info {
  text-align: left;
  font-size: 12px;
  margin: 15px 0;
  background: #f2f2f2;
  padding: 20px;
  border-radius: 10px;
}
.info i{
  padding-right: 5px;
  font-size: 15px;
  color: #9024b6;
}
.btn {
  outline: 2px solid #9024b6;
  border: none;
  padding: 10px 15px;
  cursor: pointer;
  background: transparent;
  border-radius: 8px;
}

.btn:hover {
  background: #9024b6;
  color: white;
}
</style>
