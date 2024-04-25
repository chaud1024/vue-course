<script setup>
import SlotComponent from './components/SlotComponent.vue'
import FallbackContent from './components/FallbackContent.vue'
</script>

<template>
  <SlotComponent>
    <h1>Hey there!</h1>
    <h2>Hey there!</h2>
  </SlotComponent>
  <hr />
  <FallbackContent></FallbackContent>
  <FallbackContent>
    <h3>hihihihi</h3>
  </FallbackContent>
  <hr />
  <h1>Named Slot</h1>
  <SlotComponent>
    <!--v-slot:name-->
    <template v-slot:first>
      <h1>This content will go to slot named "first"</h1>
    </template>
    <template #second>
      <h1>This content will go to slot named "second"</h1>
    </template>
  </SlotComponent>
</template>

<style scoped></style>
