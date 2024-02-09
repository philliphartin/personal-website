<template>
    <NuxtLayout>
      <NuxtPage />
    </NuxtLayout>
  </template>

  <script setup lang="ts">

  const activeBgColour = ref("#778e90")
  const bgColours = [
    "#af6f59",
    "#b36060",
    "#755e69",
    "#9e8f64",
    "#778e90",
    "#00476b",
    "#9e869e",
    "#2c4e5f",
    "#2c355f",
    "#2c5f4c",
    "#749689",
    "#495692",
  ]

  //   colourCycle({ commit, state }) {
//     const choices = state.bgColours.filter(colour => {
//       return colour !== state.activeBgColour;
//     });

//     const colour = choices[Math.floor(Math.random() * choices.length)];

</script>