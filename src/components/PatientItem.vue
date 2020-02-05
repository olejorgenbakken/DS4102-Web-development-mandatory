<template>
  <article class="patient-item">
    <section class="photo">
      <img :src="src" :alt="name" />
    </section>
    <h1>Patient {{name}}</h1>
    <h2>Disease: {{disease}}</h2>
  </article>
</template>

<script>
export default {
  name: "PatientItem",
  props: {
    name: {
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