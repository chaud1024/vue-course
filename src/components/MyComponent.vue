<script setup>
const title = 'Palermo'
const link = 'https://www.visitsicily.info/en/localita/palermo/'

const imgInfo = {
  src: 'https://images.unsplash.com/photo-1573905891290-b8e0b2d56224?q=80&w=1974&auto=format&fit=crop&ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D',
  alt: 'palermo'
}
</script>

<template>
  <div>
    <h1>{{ title }}</h1>
    <a :href="link" target="_blank" title="Go to Palermo website">
      <div class="img">
        <!-- <img :src="imgInfo.src" :alt="imgInfo.alt" /> -->
        <img :="imgInfo" />
      </div>
    </a>
  </div>
</template>

<style lang="scss" scoped>
div {
  padding: 30px;
  border-radius: 5px;
  background-color: pink;
}

h1 {
  text-align: center;
  color: darkslateblue;
}

.img {
  border-top-left-radius: 100%;
  border-top-right-radius: 100%;
  height: 700px;
  overflow: hidden;
  display: flex;
  align-items: flex-end;
  img {
    width: 100%;
  }
}
</style>
