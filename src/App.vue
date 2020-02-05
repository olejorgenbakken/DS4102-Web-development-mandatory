<template>
  <main id="main">
    <TheHeader></TheHeader>
    <PatientList></PatientList>
    <TheFooter></TheFooter>
  </main>
</template>

<script>
import TheHeader from "./layout/TheHeader";
import TheFooter from "./layout/TheFooter";
import PatientList from "./components/PatientList";
export default {
  name: "app",
  components: {
    TheHeader,
    TheFooter,
    PatientList
  }
};
</script>

<style>
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}

h1,
h2,
h3,
h4,
h5,
figcaption,
p {
  font-family: Arial, Helvetica, sans-serif;
}

img {
  max-width: 100%;
}

#main {
  width: 100%;
}
</style>
