<template>
  <article class="patient-item">
    <section class="photo">
      <img :src="src" :alt="firstName + lastName + disease" />
    </section>
    <section class="info">
      <h1>Patient: {{firstName}}</h1>
      <h2>{{lastName}}</h2>
      <h3 class="disease">Disease: {{disease}}</h3>
    </section>
  </article>
</template>

<script>
export default {
  name: "PatientItem",
  props: {
    firstName: {
      type: String,
      default: "Ola Nordmann",
      required: true
    },
    lastName: {
      type: String,
      default: "Ola Nordmann",
      required: true
    },
    src: {
      type: String,
      default: null,
      required: false
    },
    disease: {
      type: String,
      default: "Patient is sick :/ :(",
      required: true
    }
  }
};
</script>

<style scoped>
.patient-item {
  display: grid;
  grid-template-columns: 1fr;
  background: white;
  box-shadow: 0 0 5px rgba(50, 50, 50, 0.2);
  transition: 0.1s linear;
  overflow: hidden;
}

.patient-item:hover {
  transform: scale3d(1.05, 1.05, 1.05);
}

.photo {
  height: 100%;
  width: 100%;
  max-height: 200px;
}

.photo img {
  width: 100%;
  height: 100%;
  object-fit: cover;
}

.info {
  padding: 14px;
}

.disease {
  margin-top: 10px;
  color: red;
}

@media only screen and (min-width: 500px) {
  .patient-item {
    grid-template-columns: 200px 1fr;
  }
}
</style>