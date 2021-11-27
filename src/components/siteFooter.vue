<template>
  <footer>

    <div class="container-fluid">
          <div class="myContainer py-5">
              <div class="row g-3">

                  <div class="aboutUs col-3">
                      <h2 class="fs-4 fw-normal">
                          ABOUT US
                      </h2>
                      <hr style="border: 1px solid white; width: 30%; opacity: 1;">

                      <p class="fs-6 fw-light">
                          Lorem ipsum dolor sit, amet consectetur adipisicing elit. Inventore, corporis! Assumenda unde recusandae facilis obcaecati natus, aliquam dolore aperiam dicta voluptatem tenetur excepturi id libero error amet qui est inventore!
                      </p>

                      <img class="img-fluid" src="/fable/img/logo_footer.png" alt="#">
                  </div>
                  <!-- / about us -->

                   <div class="archives col-3">
                      <h2 class="fs-4 fw-normal">
                          ARCHIVES
                      </h2>
                      <hr style="border: 1px solid white; width: 30%; opacity: 1;">

                      <ul>
                          <li v-for="index in 6" :key="index" class="fs-6 fw-light mb-2">
                              MONTH (YEAR)
                          </li>
                      </ul>

                  </div>
                  <!-- / ARCHIVIO -->

                   <div class="features col-3">
                      <h2 class="fs-4 fw-normal">
                          OUR FEATURES
                      </h2>
                      <hr style="border: 1px solid white; width: 30%; opacity: 1;">
                      
                      <p class="fs-6 fw-light">
                        Lorem ipsum dolor sit amet consectetur adipisicing elit. Reiciendis, dolorem?
                      </p>

                      <ul>
                          <li v-for="index in 6" :key="index" class="fs-6 fw-light mb-2">
                             <img class="me-2" src="/fable/img/style_4_alt.png" alt="#">  friendly and welcoming place
                          </li>
                      </ul>

                  </div>
                  <!-- / OUR FEATURES -->

                  <div class="posts col-3">
                      <h2 class="fs-4 fw-normal">
                          RECENT POSTS
                      </h2>
                      <hr class="mb-4" style="border: 1px solid white; width: 30%; opacity: 1;">
                      
                      <div v-for="index in 3" :key="index" class="col-12 d-flex align-items-center">
                          <div class="col-6">
                              <img style="width:100%" src="/fable/img/gallery_03.jpg" alt="#">
                          </div>
                          <div class="col-6 p-2">
                              <p class="fs-5">
                                  drawing and painting lessons
                              </p>

                              <p class="fs-6 fw-light">
                                  <img class="me-2" src="/fable/img/date_footer.png" alt="#">
                                  october 02 2014
                              </p>
                          </div>
                      </div>
                  </div>
                  <!-- / RECENT POSTS -->
              </div>
          </div>
    </div>

    <div class="myContainer">
        <div class="row pt-5 justify-content-center">
              <div class="text-center pb-3">
                 <img v-for="index in 5" :key="index" class="bgOrange me-1" src="/fable/img/facebook.png" alt="#">
              </div>
              <div>
                  <p class="fs-6 descr text-center">
                     &#169; fable- children kindergarten Lorem, ipsum. 
                  </p>
              </div>
        </div>
    </div>

    <div class="icon">
        <a href="#header"> <img src="/fable/img/go_to_top.png" alt="#"> </a> 
    </div>
  </footer>
</template>

<script>
export default {

}
</script>

<style lang="scss">
  footer {
    ul {
      padding: 0!important;
      list-style-type: none;
    }

    .container-fluid {
      background-image: url("/fable/img/pattern.png");
      color: white;

      .archives {
        ul {
          list-style-type: none;
          width: 100%;
          padding: 0;
          li {
            width: 100%;
            border: 1px solid white;
            padding: 0.3rem 1rem;
          }
        }


      }
      /* / archives */

      .posts {
        p {
          line-height: 1.1;
          margin-bottom: 0.4rem;
        }
      }
    }

    .icon {
      position: fixed;
      bottom: 0;
      right: 0;
      padding: 1rem;
      
      img {
        background-color: rgba(0, 0, 0, 0.322);
      }
    }
  }
</style>