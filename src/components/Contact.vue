<script setup lang="ts">
import { ref } from 'vue';

const formData = ref({
  name: '',
  email: '',
  message: ''
});

const handleSubmit = () => {
  console.log('ទិន្នន័យដែលបានផ្ញើ:', formData.value);
  alert('សូមអរគុណ! សាររបស់អ្នកត្រូវបានផ្ញើ។');
};
</script>

<template>
  <div class=" contact-card shadow-sm">
    <div class="d-flex align-items-center mb-4">
      <h2 class="fw-bold m-0">Contact</h2>
      <div class="title-line ms-4"></div>
    </div>

    <div class="row g-4 mb-5">
      <div class="col-12 col-md-6">
        <div class="info-box h-100 d-flex align-items-start p-4 rounded-4 bg-light-orange">
          <div class="icon-circle me-3">
           <i class="iconoir-smartphone-device"></i>
          </div>
          <div>
            <p class="text-muted mb-1"> Phone:</p>
            <p class="fw-bold mb-0">+855 93374929</p>
          </div>
        </div>
      </div>

      <div class=" col-12 col-md-6">
        <div class="info-box h-100 d-flex align-items-start p-4 rounded-4 bg-light-blue">
          <div class="icon-circle me-3">
           <i class="iconoir-mail-open"></i>
          </div>
          <div>
            <p class="text-muted mb-1"> Email:</p>
            <p class="fw-bold mb-0">sokleangchieang123@gmail.com</p>
          </div>
        </div>
      </div>
    </div>

    <div class="form-container p-3 rounded-4 border">
      <p class="mb-2">
        I am always open to discussing <strong>new projects, opportunities in tech world, partnerships</strong> and more so <strong>mentorship</strong>.
      </p>
      
      <form @submit.prevent="handleSubmit">
        <div class="mb-2 border-bottom">
          <label class="form-label text-muted small mb-0">Name:</label>
          <input v-model="formData.name" type="text" class="form-control border-0 px-0 shadow-none" required>
        </div>

        <div class="mb-2 border-bottom">
          <label class="form-label text-muted small mb-0">Email:</label>
          <input v-model="formData.email" type="email" class="form-control border-0 px-0 shadow-none" required>
        </div>

        <div class="mb-2 border-bottom">
          <label class="form-label text-muted small mb-0">Message:</label>
          <textarea v-model="formData.message" class="form-control border-0 px-0 shadow-none" rows="1" required></textarea>
        </div>

        <button type="submit" class="btn btn-outline-dark  px-4 mt-2">Submit</button>
      </form>
    </div>
  </div>
</template>

<style scoped>
.contact-card {
  background: white;
  border-radius: 20px;
  padding: 30px;
  /* min-height: 100%; */
  min-height: 80vh; /* ពេញអេក្រង់ទូរស័ព្ទ និង PC */
  width: 100%;
}

.title-line {
  height: 2px;
  width: 150px;
  background-color: #9024b6;;
}

.bg-light-orange { background-color: #ddbbe8; }
.bg-light-blue { background-color: #eedef4; }

.icon-circle {
  /* color: #9024b6; */
  font-size: 1.5rem;
}

.form-control:focus {
  background-color: transparent;
}
.form-control:hover{
  cursor: pointer;
} 
/* @media (min-width: 768px) {
  .row .info-box {
  
  }
} */

.form-container {
  background-color: #fcfcfc;

}
/* .info-box{
  word-break: break-word;
} */

/* លុប Border របស់ input ឱ្យឃើញតែបន្ទាត់ខាងក្រោម*/
input, textarea {
  border-radius: 0;
  background-color: transparent;
}

/* ប៊ូតុង Submit */
.btn-outline-dark {
  border: 1px solid #ddd;
  transition: 0.3s;
  outline: 2px solid #9024b6;
}

.btn-outline-dark:hover {
  background-color: #9024b6;;
  border-color: #9024b6;;
  color: white;
  cursor: pointer;
}
</style>