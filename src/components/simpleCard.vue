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
    .welcomeCard {
              text-align: center;
                  
                  .img {
                        width: 150px;
                        height: 150px;
                        margin: auto;
                        position: relative;
                  }

                  img {
                    padding: 1rem;
                    position: absolute;
                    left: 50%;
                    top: 50%;
                    transform: translate(-50%, -50%);
                    width: 100px;
                  }
            }
</style>