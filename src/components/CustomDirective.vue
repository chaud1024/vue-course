<script setup>
const vFormateDiv = {
  mounted: (el, binding) => {
    console.log(el)
    console.log(binding.value)

    // el.style.fontSize = binding.value + 'px'
    el.style.fontSize = `${binding.value}px`
    el.style.color = 'crimson'
    el.style.backgroundColor = 'lightblue'
  }
}

const vAnotherFormateDiv = {
  mounted: (el, binding) => {
    console.log(binding.arg)

    switch (binding.arg) {
      case 'orange':
        el.style.color = 'orange'
        break
      case 'pink':
        el.style.color = 'pink'
        break
      case 'teal':
        el.style.color = 'teal'
        break

      default:
        el.style.color = 'black'
    }
  }
}
</script>

<template>
  <div>
    <h1>Custom Directive</h1>
    <div v-formate-div="30">Using simple custom directive</div>
    <div v-another-formate-div:orange>This uses another custom directive</div>
    <div v-another-formate-div:teal>This uses another custom directive</div>
    <div v-another-formate-div:pink>This uses another custom directive</div>
    <div v-another-formate-div>This uses another custom directive</div>
  </div>
</template>

<style lang="scss" scoped></style>
