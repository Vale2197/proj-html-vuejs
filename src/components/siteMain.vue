<template>
  <main>
    <section id="welcomeToFable">
        <div class="jumboImage">
        </div>
        <!-- /hero image -->

        <div class="jumboText">

            <div class="myContainer">
              <div class="row justify-between">
                <div class="col">
                   <p>
                  Lorem, ipsum dolor.
                  </p>
                </div>

                <div class="col text-end">
                    <button>
                        learn more
                    </button>
                </div>
               
              </div>
            </div>

        </div>
        <!-- / jumbo txt -->

        <div class="welcome py-5">
            <div class="myContainer">

              <div class="row justify-between">
                  <div class="col-12">
                    <h2>
                        WELCOME
                    </h2>
                  </div>
                  <!-- /title -->
                  <div class="col-3">contents</div>
                  <div class="col-3">contents</div>
                  <div class="col-3">contents</div>
                  <div class="col-3">contents</div>
              </div>
              <!-- / row -->
            </div>
        </div>
        <!-- / WELCOME -->

        <div class="overview py-5">
          <div class="myContainer">

              <div class="row">
                  <div class="col-6">
                    textHere
                  </div>
                  <!-- 
                    / txt e overview
                   -->
                  <div class="col-6">
                    <div class="row">
                      <div class="col-12">
                          ACTIVE-IMG
                      </div>
                      <div class="col-4">
                        other imgs
                      </div>
                      <div class="col-4">
                        other imgs
                      </div>
                      <div class="col-4">
                        other imgs
                      </div>
                    </div>
                    <!-- / row -->
                  </div>
                  <!-- 
                    / slide IMAGES
                   -->
              </div>

          </div>
        </div>
        <!-- / OVERVIEW -->
    </section>
    <!-- 
       / WELCOME TO FABLE
     -->




    <section id="ourClass">

      <div class="jumboImage">
          <div class="myContainer">
              <div class="row">
                  <div class="col-3">rounded-contents</div>
                  <div class="col-3">rounded-contents</div>
                  <div class="col-3">rounded-contents</div>
                  <div class="col-3">rounded-contents</div>
              </div>
          </div>
      </div>
      <!-- / JUMBO IMAGE -->

      <div class="classes">
          <div class="myContainer">
              <div class="row g-2 py-3">

                  <div class="title col-12 text-center">
                      <h2>
                          OUR CLASSES
                      </h2>
                  </div>
                  <!-- / title -->

                  <div class="col-6">
                      <p>
                          descript.
                      </p>
                  </div>
                  <!--  -->

                  <div class="col-6">
                      <p>
                          descript.
                      </p>
                  </div>
                  <!--  -->

                  <div class="col-6">
                    <div class="card">
                        cards imgs
                    </div>
                  </div>

                  <div class="col-6">
                    <div class="card">
                        cards imgs
                    </div>
                  </div>

                  <div class="col-6">
                    <div class="card">
                        cards imgs
                    </div>
                  </div>

                  <div class="col-6">
                    <div class="card">
                        cards imgs
                    </div>
                  </div>
                  <!-- / cards -->

              </div>
          </div>
      </div>
      <!--  / CLASSES DESCR. -->

      <div class="aboutUs">
          <div class="myContainer">

            <div class="row py-5">
                <div class="col-6">
                  Lorem ipsum dolor sit amet consectetur, adipisicing elit. Minus quaerat magnam perspiciatis voluptatem dicta quo illo, delectus eum impedit sapiente esse numquam cum, nostrum quasi quis quisquam earum non nam.
                </div>
              <!-- text -->

                <div class="col-6">

                    <div class="icons row">
                        <div class="col-6">
                          <p>
                            rounded icons
                          </p>
                        </div>
                        <div class="col-6">
                          <p>
                            rounded icons
                          </p>
                        </div>
                        <div class="col-6">
                          <p>
                            rounded icons
                          </p>
                        </div>
                        <div class="col-6">
                          <p>
                            rounded icons
                          </p>
                        </div>
                    </div>
                </div>
                <!-- / icons -->

            </div>
            <!-- / row -->
          </div>
      </div>
      <!-- / about us -->

    </section>
    <!-- 
        / OUR CLASS
     -->
     



    <section id="ourStaff">
        <div class="jumboImage"></div>

        <div class="jumboText">

            <div class="myContainer">
                <div class="row">

                    <div class="col">
                      textHere
                    </div>

                    <div class="col text-end">
                        <button>
                            more
                        </button>
                    </div>

                </div>
            </div>

        </div>
        <!-- /jumboText -->

        <div class="meetUs">
            <div class="myContainer text-center">
                <div class="row">

                    <div class="col-12">
                        <h2>
                            TITLE MEET US
                        </h2>
                    </div>
                    <!-- / title -->

                    <div class="col-6">
                        description
                    </div>
                    <div class="col-6">
                        description
                    </div>
                </div>
                <!-- / row -->

                <div class="row py-3">
                    <div class="col-6">
                        cards and imGs
                    </div>
                    <div class="col-6">
                        cards and imGs
                    </div>
                    <div class="col-6">
                        cards and imGs
                    </div>
                    <div class="col-6">
                        cards and imGs
                    </div>
                </div>
                <!-- / row 2 -->
            </div>
        </div>
    </section>
    <!-- 
        / OUR STAFF
     -->

    <section id="news">
    </section>
    <!-- 
        / NEWS
     -->

    <section id="contactUs">
    </section>
    <!-- 
        / CONTACT US
     -->
  </main>
</template>

<script>
export default {

}
</script>

<style lang="scss">
  main {

      .jumboImage {
          width: 100%;
          height: 400px;
          background-color: greenyellow;
      }
      #welcomeToFable {
          .jumboText {
            background-color: cornflowerblue;
          }

          .welcome {
            text-align: center;
            .col-3 {
              text-align: center;
            }
          }
          .overview {
            background: rgb(214, 214, 214);
          }
      }
    /* 
        / welcomeToFable
    */

      #ourClass {
        .myContainer {
          height: 100%;

            .row {
              height: 100%;
              align-items: center;
            }
        }
        
        .classes {
            .card {
              background-color: cornflowerblue;
              height: 100px;
            }
        }

        .aboutUs {
            background-color: rgb(224, 224, 224);
          .icons p{
            background-color: darkgoldenrod;
          }
        }
      }
      /* 
          / OUR CLASS
      */

      #ourStaff {
        .jumboText {
          background-color: lightcoral;
        }
      }
  }
</style>