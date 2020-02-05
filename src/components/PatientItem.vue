<template>
  <article class="patient-item">
    <section class="photo">
      <img :src="src" :alt="name" />
    </section>
    <section>
      <h1>Patient: {{firstName}}</h1>
      <h2>{{lastName}}</h2>
      <h3>Disease: {{disease}}</h3>
    </section>
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

<style scoped>
.patient-item {
  display: grid;
}
</style>