<template>
  <main>
    <section id="welcomeToFable">
        <div class="jumboImage position-relative">
          <img class="trenino" src="/fable/img/slider_slide3_img2.png" alt="#">
          <img class="lego" src="/fable/img/slider_slide3_img3.png" alt="#">
          <div class="slideBars">
              <div class="bar" v-for="index in 3" :key="index"></div>
          </div>
        </div>
        <!-- /hero image -->

        <div class="jumboText">

            <div class="myContainer">
              <div class="row justify-between">
                <div class="col">
                  <p>
                      How to Enroll your Child to a Class?   
                  </p>
                </div>

                <div class="col justify-content-end">
                    <button class="btn">
                        learn more <img style="width: 2rem" src="/fable/img/slider_next.png" alt="">
                    </button>
                </div>
               
              </div>
            </div>

        </div>
        <!-- / jumbo txt -->

        <div class="welcome py-5">
            <div class="myContainer">

              <div class="row justify-between">
                  <div class="title col-12 pb-5">
                      <h2 class="fs-1 fw-light">
                          Welcome to Fable
                      </h2>

                      <p class="fs-6 py-3">
                          Fable daycare, preschool and kindergarten
                      </p>

                      <img src="/fable/img/header_divider.png" alt="#">
                  </div>
                  <!-- /title -->
                  
                  <simpleCard v-for="(card, index) in welcomeCards" :key="index" :class="'col-3'" 
                  :image="card.img" 
                  :imgClass="'rounded-circle' +  pari(index)"
                  :titolo="card.title" 
                  :description="card.paragraph" />
                      
              </div>
              <!-- / row -->
            </div>
        </div>
        <!-- / WELCOME -->

        <div class="overview py-5">
          <div class="myContainer">

              <div class="row py-3 align-items-center">
                  <div class="col-6">
                      <button class="btn bgOrange mb-4">
                          Overview
                      </button>
                      <button class="unactive btn mb-4">
                          Our Mission
                      </button>
                      <p class="title fs-4 mb-4">
                          Lorem ipsum dolor sit amet consectetur adipisicing elit. Neque, officia?
                      </p>
                      <!-- / overview title -->


                      <div class="description d-flex mb-3">

                          <div class="me-3">
                            <div class="img rounded-circle bgOrange">
                                <img src="/fable/img/clock_alt.png" alt="#">
                            </div>
                          </div>
                          
                          <div class="txt">
                              <p class="title fs-5 mb-1">
                                  Full day session
                              </p>
                              <p class="fs-6 descr">
                                  Lorem, ipsum dolor.
                              </p>
                          </div>
                      </div>
                      <!--  -->

                      <div class="description d-flex">
                          <div class="me-3">
                            <div class="img rounded-circle bgOrange">
                                <img src="/fable/img/diagram_alt.png" alt="#">
                            </div>
                          </div>
                          
                          <div class="txt">
                              <p class="fs-5 mb-1 title">
                                  Full day session
                              </p>
                              <p class="descr fs-6">
                                  Lorem, ipsum dolor.
                              </p>
                          </div>
                      </div>
                    <!-- / DESCRIPTION -->
                  </div>
                  <!-- 
                    / txt e overview
                   -->
                  <div class="col-6">
                    <div class="row g-2">
                      <div class="col-12 position-relative">
                          <img class="img-fluid" src="/fable/img/gallery_01.jpg" alt="#">
                          <img class="nextSlide position-absolute top-50 end-0 " src="/fable/img/slider_next.png" alt="#">
                          <img class="prevSlide position-absolute top-50 start-0 " src="/fable/img/slider_previous.png" alt="#">
                      </div>
                      <div class="col-4 pb-2">
                        <img class="img-fluid" src="/fable/img/gallery_01.jpg" alt="#">
                      </div>
                      <div class="slideActiveImg col-4 pb-2">
                        <img class="img-fluid" src="/fable/img/gallery_01.jpg" alt="#">
                      </div>
                      <div class="col-4 pb-2">
                        <img class="img-fluid" src="/fable/img/gallery_01.jpg" alt="#">
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
        <div class="jumboImage">
            <div class="myContainer">
                <div class="row text-center">
                    <div class="col-12">
                        Lorem ipsum dolor sit amet, consectetur adipisicing elit. Ea, soluta.
                    </div>
                </div>
            </div>
        </div>
        <!-- / jumbo img -->

        <div class="whatsNew">
            <div class="myContainer py-5 text-center">
                <div class="row">
                    <div class="col-12">
                        <h2>
                            TITLE NEWS
                        </h2>
                    </div>
                </div>
                <!-- / TITLE -->
                <div class="row">
                    <div class="col-4">
                        cards
                    </div>
                    <div class="col-4">
                        cards
                    </div>
                    <div class="col-4">
                        cards
                    </div>
                    <!-- / cards -->
                    <div class="col-12">
                        <button>
                            button
                        </button>
                    </div>
                </div>
                <!-- / CARDS -->
            </div>
        </div>
        <!-- / WHATS NEW -->
    </section>
    <!-- 
        / NEWS
     -->

    <section id="contactUs">
        <div class="jumboImage"></div>
        <!-- / jumbo img -->

        <div class="contact">
             <div class="myContainer">
                  <div class="row">

                      <div class="title col-12 text-center">
                          <h2>
                              CONTACT US
                          </h2>
                      </div>
                      <!-- / title -->

                      <div class="col-3"> CARDS </div>
                      <div class="col-3"> CARDS </div>
                      <div class="col-3"> CARDS </div>
                      <div class="col-3"> CARDS </div>
                      <!-- / cards -->

                      <div class="userContact col-6">
                          contact form
                      </div>
                      <div class="txtArea col-6">
                          text area
                      </div>
                      <!-- / form -->
                      <div class="text-center col-12">
                          <button>
                              send
                          </button>
                      </div>
                  </div>
                  <!-- / row -->
             </div>
        </div>
    </section>
    <!-- 
        / CONTACT US
     -->
  </main>
</template>

<script>
import simpleCard from "./simpleCard.vue";
export default {
    components: {
      simpleCard
    },

    data() {
      return {
          welcomeCards: [
            {
              title: 'Morbi Etos',
              paragraph: ' Lorem ipsum dolor sit amet consectetur adipisicing elit. Perferendis qui omnis debitis eaque non et laudantium ipsum, quod dignissimos nihil.',
              img: '/fable/img/schoolbag_alt.png'
            },
            {
              title: 'Congue Gravida',
              paragraph: ' Lorem ipsum dolor sit amet consectetur adipisicing elit. Perferendis qui omnis debitis eaque non et laudantium ipsum, quod dignissimos nihil.',
              img: '/fable/img/stroller_alt.png'
            },
            {
              title: 'Maecenas Node',
              paragraph: ' Lorem ipsum dolor sit amet consectetur adipisicing elit. Perferendis qui omnis debitis eaque non et laudantium ipsum, quod dignissimos nihil.',
              img: '/fable/img/globe_alt.png'
            },
            {
              title: 'Praesent Morbi',
              paragraph: ' Lorem ipsum dolor sit amet consectetur adipisicing elit. Perferendis qui omnis debitis eaque non et laudantium ipsum, quod dignissimos nihil.',
              img: '/fable/img/bell_alt.png'
            }
          ],
          
      }
    },

    methods: {
      pari(index) {
        if(index % 2 != 0) {
          return ' bgPurple'
        }
        else{
          return ' bgOrange'
        }
      }
    }
}
</script>

<style lang="scss">
  main {
        
        .title {
          color:  #56509f;
        }

      
        .descr {
                  color: grey;
                }
        

       .bgPurple {
                       background-color: #56509f ;
                  }

        .bgOrange {
          background-color: #fd6500 ;
        }

      .jumboImage {
          width: 100%;
          height: 400px;
      }
      #welcomeToFable {
          .jumboImage {
              background-image: url("/fable/img/slider_slide3_background.png");
              background-repeat: repeat;
              background-size: contain;

              .slideBars {
                    display: flex;
                    position: absolute;
                    bottom: 1rem;
                    left: 50%;
                    transform: translate(-50%);

                    .bar {
                        width: 2rem;
                        height: 0.7rem;
                        margin: 0 0.5rem;
                        border: 3px solid orange;
                    }
              }
              
              .trenino {
                  position: absolute;
                  bottom: 3rem;
                  left: 50%;
                  transform: translate(-50%, 0);
                  width: 200px;
              }

              .lego {
                position: absolute;
                left: 80%;
                bottom: 3rem;
                width: 150px;
              }
          }

          /* 
              / JUMBO IMAGE
          */
          .jumboText {
            background-image: url("/fable/img/pattern.png");

              .col {
                height: 5rem;
                display: flex;
                align-items: center;

                p {
                  margin: 0;
                  font-size: 1.5rem;
                  color: white;
                }

                button {
                      border: 2px solid white;
                      color: white;
                      border-radius: 0;
                }
              }
          }
          /*  / jumbo text */

          .welcome {
            text-align: center;
            .title {
              h2 {
              color:  #56509f;
              }

              p {
                color: grey;
              }
            }
            /* / title */
            
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
          }
          /* / WELCOME */



          .overview {
            background: #f5f5f5;
           
            button {
              color: white;
              border-radius: 0;
            }

            button.unactive {
              color: grey;
              border-bottom: 1px solid gray;
              margin-left: 1rem;
            }
            .img {
              padding: 1rem;
              img {
                width: 1.5rem;
              }
            }
            
            /* / OVERVIEW TEXT */
            .nextSlide {
                transform: translate(0, -50%);
                background-color: #fd6500;
            }

            .prevSlide {
                transform: translate(0, -50%);
                background-color: #fd6500;
            }

            .slideActiveImg {
              border-bottom: 2px solid #fd6500;
            }
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
      /* 
          / OUR STAFF
      */

      #news {
        .myContainer {
          height: 100%;
          .row {
            height: 100%;
            align-items: center;
          }
        }
      }
  }
</style>