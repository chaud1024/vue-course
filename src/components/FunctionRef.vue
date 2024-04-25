<script setup>
const myRefFunc = (el) => {
  console.log(el.textContent) // Reading text content
  el.textContent = 'This is an updated value'
  el.style.color = 'crimson'
}
</script>

<template>
  <div>
    <h1>Function Ref</h1>
    <h2 :ref="myRefFunc">This is an initial value</h2>
  </div>
</template>

<style lang="scss" scoped></style>
