<template>
  <div class="welcomeCard" :class="myclass">
      <div class="img mb-3" :class="imgClass">
        <img :src="image" alt="#">
      </div>
      <p class="title fs-5 fw-normal">
          {{titolo}}
      </p>
      <p class="fs-6 descr">
          {{description}}
      </p>
  </div>
</template>

<script>
export default {
    props: {
        image: String,
        titolo: String,
        description: String,
        myclass: String,
        imgClass: String
    }
}
</script>

<style lang="scss">

</style>