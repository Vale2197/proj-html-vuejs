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
    </section>
    <!-- 
        / OUR CLASS
     -->
     
    <section id="ourStaff">
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
  #welcomeToFable {
      .jumboImage {
          width: 100%;
          height: 400px;
          background-color: greenyellow;
      }
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

</style>