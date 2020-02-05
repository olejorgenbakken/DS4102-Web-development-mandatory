<template>
  <section class="patient-list">
    <PatientItem
      v-for="patient in patients"
      :key="patient.name"
      :name="patient.name"
      :disease="patient.disease"
      :src="patient.img"
    ></PatientItem>
  </section>
</template>

<script>
import patients from "../assets/patients";
import PatientItem from "./PatientItem";

export default {
  name: "PatientList",
  data() {
    return patients;
  },
  components: {
    PatientItem
  }
};
</script>

<style>
.patient-list {
  width: 100%;
  max-width: 1000px;
  display: grid;
  grid-template-columns: repeat(3, 1fr);
  margin: 0 auto;
  gap: 20px;
}
</style>