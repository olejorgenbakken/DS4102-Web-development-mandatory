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

h1 {
  font-size: 2em;
}

h2 {
  font-size: 1.5em;
}

h3 {
  font-size: 1.2em;
}

img {
  max-width: 100%;
}

#main {
  width: 100%;
  background: lightgrey;
}
</style>
