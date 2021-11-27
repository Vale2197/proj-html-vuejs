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

                      <img class="imgColor" src="/fable/img/header_divider.png" alt="#">
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
        <div class="overlay">
          <div class="myContainer">
              <div class="row">
                <!-- cerchi -->
                  <div v-for="index in 4" :key="index" class="col-3 text-center">
                      <div class="img imgColor mb-2">
                          <span class="fs-1 fw-light">
                              500
                          </span>
                      </div>

                      <div class="txt">
                          <p class="fs-4">
                              Lorem, ipsum.
                          </p>
                          <p class="fs-6">
                              Lorem ipsum dolor sit, amet consectetur adipisicing elit.
                          </p>
                      </div>
                  </div>
                  <!-- / cerchio -->
                  <div class="col-12 d-flex justify-content-center">
                      <div v-for="index in 6" :key="index" class="slideBars">
                      </div>
                  </div>
              </div>
          </div>
        </div>
      </div>
      <!-- / JUMBO IMAGE -->

      <div class="classes">
          <div class="myContainer pb-4">
              <div class="row py-5">

                  <div class="title col-12 text-center mb-5">
                      <h2 class="fs-1 fw-light">
                          Our Classes
                      </h2>
                      <p class="fs-6 descr">
                          Lorem ipsum dolor sit.
                      </p>
                      <img class="imgColor" src="/fable/img/header_divider.png" alt="#">
                  </div>
                  <!-- / title -->

                  <div class="col-6">
                      <p class="fs-4 title">
                          Lorem ipsum dolor sit amet consectetur adipisicing elit. Dolorum quis ea modi vero, facere ipsum.
                      </p>
                  </div>
                  <!-- / paragraph -->

                  <div class="col-6">
                      <p class="fs-6 descr">
                          Lorem ipsum dolor sit amet consectetur adipisicing elit. Harum, nostrum. Magni veniam beatae asperiores dignissimos aliquam quos fuga facere illo.
                      </p>
                  </div>
                  <!-- / description -->

                  <!-- card -->
                  <div class="row g-3 pt-4">
                      <div v-for="index in 4" :key="index" class="col-6 d-flex">
                          <div class="myCard col-6 d-flex flex-wrap ">
                              <div class="pt-3 ps-3 col-12 mb-5">
                                  <p class="fs-4">
                                     Little Lambs
                                  </p>
                                  <p class="fs-6 fw-light">
                                    Class Name
                                  </p>
                              </div>
                              <!-- / title -->

                              <div class=" yearsCol col-6 mb-2 text-center">
                                  <p class="fs-5">
                                     12-24
                                  </p>
                                  <p class="fs-6 fw-light">
                                      Month old
                                  </p>
                              </div>
                              <!-- / years -->

                              <div class="col-6 mb-2 text-center ">
                                 <p class="fs-5">
                                     9
                                  </p>
                                  <p class="fs-6 fw-light">
                                      Class size
                                  </p>
                              </div>
                              <!-- / class size -->
                          </div>

                          <div class="col-6 position-relative">
                              <img src="/fable/img/gallery_04.jpg" alt="#">
                              <button class="btn position-absolute bottom-0 end-0 bgOrange d-flex align-items-center">
                                  READ MORE
                                  <img style="width: 2rem" src="/fable/img/slider_next.png" alt="#">
                              </button>
                          </div>
                          <!-- / card image -->
                      </div>
                  <!-- / card -->
                  </div>
                  

              </div>
          </div>
      </div>
      <!--  / CLASSES DESCR. -->

      <div class="aboutUs">
          <div class="myContainer">

            <div class="row py-5 align-items-start">
                <div class="col-6">
                    <h2 class="title fs-4 fw-normal">
                        Lorem ipsum dolor sit amet consectetur adipisicing elit. Iusto, quasi quis deleniti esse nam ut veritatis. Obcaecati, laudantium a debitis et consectetur est
                    </h2>
                    <p class="fs-6 descr py-5">
                        Lorem ipsum dolor sit amet consectetur adipisicing elit. Nesciunt incidunt enim minus. Provident quaerat voluptatem error recusandae rerum totam ipsa?
                    </p>
                    <ul class="p-0">
                        <li v-for="index in 6" :key="index" class="fs-6 descr mb-2">
                            <img class="me-2 imgColor" src="/fable/img/style_1.png" alt="#"> Lorem ipsum dolor sit amet consectetur.
                        </li>
                    </ul>
                </div>
              <!-- text -->

                <div class="col-6">

                    <div class="icons row">
                        <div class="col-6 text-center mb-3" v-for="index in 4" :key="index">
                              <div class="img imgColor mb-3 position-relative">
                                <img class="position-absolute top-50 start-50 translate-middle" src="/fable/img/toy.png" alt="#">
                              </div>
                              <p class="title fs-5 fw-normal">
                                  Lorem, ipsum dolor.
                              </p>
                              <p class="fs-6 descr">
                                  Lorem ipsum dolor, sit amet consectetur adipisicing elit.
                              </p>
                        </div>
                        <!-- /aboutUs card -->

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

                    <div class="col fs-3 fw-light">
                      See our Kindergarten Photo Gallery
                    </div>

                    <div class="col justify-content-end">
                        <button class="btn">
                            View Gallery <img style="width: 2rem" src="/fable/img/slider_next.png" alt="#">
                        </button>
                    </div>

                </div>
            </div>

        </div>
        <!-- /jumboText -->

        <div class="meetUs">
            <div class="myContainer">
                <div class="row py-5">

                    <div class="col-12 mb-5 text-center">
                        <h2 class="fs-1 fw-light">
                          Meet Our Staff
                        </h2>
                        <p class="fs-6 descr">
                            Lorem ipsum dolor sit.
                        </p>
                        <img class="imgColor" src="/fable/img/header_divider.png" alt="#">
                    </div>
                    <!-- / title -->

                    <div class="col-6">
                      <p class="fs-4 title">
                          Lorem ipsum dolor sit amet consectetur adipisicing elit. Dolorum quis ea modi vero, facere ipsum.
                      </p>
                    </div>
                    <!-- / paragraph -->

                    <div class="col-6">
                      <p class="fs-6 descr">
                          Lorem ipsum dolor sit amet consectetur adipisicing elit. Harum, nostrum. Magni veniam beatae asperiores dignissimos aliquam quos fuga facere illo.
                      </p>
                  </div>
                  <!-- / description -->
                </div>
                <!-- / row -->

                <div class="row py-4 g-4">

                  <!-- card -->
                    <div v-for="index in 4" :key="index" class="myCard col-6 d-flex">
                        <div class="col-6 text-center">
                            <img class="img-fluid" src="/fable/img/gallery_08-690x506.jpg" alt="#">
                            <p class="fs-5 title m-0 mt-3">
                                Name T.
                            </p>
                            <p class="fs-6 descr">
                                teacher
                            </p>
                        </div>
                        <!-- /teacher name -->

                        <div class="col-6 description">
                            <div class="img">
                                <img class="imgColor btn" src="/fable/img/quote.png" alt="#">
                            </div>
                            <p class="fs-6 descr">
                                Lorem ipsum dolor, sit amet consectetur adipisicing elit. Explicabo accusantium veniam nesciunt hic, sit molestiae?
                            </p>
                            <div class="icons">
                                <img class="bgOrange" src="/fable/img/mail.png" alt="#">
                                <img class="bgOrange" src="/fable/img/facebook.png" alt="#">
                                <img class="bgOrange" src="/fable/img/pinterest.png" alt="#">
                            </div>
                        </div>
                    </div>
                    <!-- / card -->
                </div>
                <!-- / row 2 -->
            </div>
        </div>
    </section>
    <!-- 
        / OUR STAFF
     -->





    <section id="news" class="py-4">
        <div class="jumboImage">

            <div class="overlay">

                <div class="myContainer">

                    <div class="row text-center">
                        <div class="col-12">
                            <div class="img mb-4">
                                <img src="/fable/img/quote_alt.png" alt="#">
                            </div>
                            <!-- /quotes  -->

                            <p class="fs-4 fw-light">
                                Lorem ipsum dolor sit amet consectetur adipisicing elit. Commodi assumenda eaque quisquam harum, obcaecati repellat nihil exercitationem deleniti reprehenderit sit dolores distinctio aliquam placeat impedit nesciunt cumque hic sequi labore.
                            </p>
                            <hr style="width: 10%; margin: auto">
                            <p class="fs-6 fw-bold">
                                J. Lorem
                            </p>
                            <!-- / description -->

                            <div style="width: 100%;" class="slideBars d-flex justify-content-center mt-4">
                                <div v-for="index in 6" :key="index" class="bar"></div>
                            </div>
                        </div>
                    </div>

                </div>
            </div>
            <!-- / overlay -->
        </div>
        <!-- 
          / jumbo img   
        -->

        <div class="whatsNew">
            <div class="myContainer py-5 text-center">
                <div class="row">
                    <div class="col-12 pb-5">
                        <h2 class="fs-1 fw-light title">
                            What's New
                        </h2>

                        <p class="fs-6 descr">
                          Lorem ipsum dolor sit.
                        </p>

                        <img class="imgColor" src="/fable/img/header_divider.png" alt="#">
                    </div>
                </div>
                <!-- / TITLE -->

                <div class="row g-3 pb-5">

                  <!-- card -->
                    <div v-for="index in 3" :key="index" class="myCard col-4">
                        <p class="fs-6 descr">
                            October 03, 2014
                        </p>
                        <div class="img">
                            <img src="/fable/img/gallery_03.jpg" alt="#">
                            <p>
                                42
                            </p>
                        </div>
                        <!-- / img -->

                        <p class="fs-5 title mt-3">
                            Lorem ipsum dolor sit.
                        </p>

                        <p class="fs-6 descr">
                            Lorem ipsum dolor sit amet consectetur adipisicing elit. Numquam quam quos similique fugiat, nisi nemo. Vitae, nemo vero. Id corrupti a assumenda eos impedit, consequatur magnam saepe? Quas, qui laudantium.
                        </p>
                        <hr>

                        <!-- / description -->

                        <div class="otherCont d-flex">
                            <div class="col-6">
                                <p class="fs-6 descr">
                                  <img src="/fable/img/author.png" alt="#">
                                  Anna Lorem
                                </p>
                            </div>

                            <div class="col-6">
                                <p class="fs-6 descr ps-3">
                                    <img src="/fable/img/category.png" alt="#">
                                    Events, fun
                                </p>
                            </div>
                        </div>

                    </div>
                    <!-- / card-->


                    <div class="col-12 pt-5">
                        <button class="btn bgOrange">
                            button 
                            <img style="width: 2rem" src="/fable/img/slider_next.png" alt="#">
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
        <div class="jumboImage position-relative mb-5">
            <img src="/fable/map.png" alt="#">
            <i class="fas fa-map-marker-alt"></i>
        </div>
        <!-- / jumbo img -->

        <div class="contact">
             <div class="myContainer">
                  <div class="row pb-5">

                      <div class="col-12 mb-5 text-center">
                          <h2 class="fs-1 fw-light">
                            Contact Us
                          </h2>
                          <p class="fs-6 descr">
                              Lorem ipsum dolor sit.
                          </p>
                          <img class="imgColor" src="/fable/img/header_divider.png" alt="#">
                      </div>
                      <!-- / title -->

                      <!-- card -->
                      <div class="col-3 myCard" v-for="index in 4" :key="index"> 
                            <div class="text-center mb-3">
                                <div class="img mb-3 ">
                                  <img class="imgColor" src="/fable/img/clock.png" alt="#">
                                </div>
                                <p class="title fs-5 fw-normal">
                                    Lorem, ipsum dolor.
                                </p>
                                <p class="fs-6 descr">
                                    Lorem ipsum dolor, sit amet consectetur adipisicing elit.
                                </p>
                            </div>
                      </div>
                      <!-- / card -->


                      <div class="row pt-5">
                          <div class="userContact col-6">
                              <label for="name" class="position-relative">
                                  <input class="form-control" type="text" placeholder="Your Name *">
                                  <img class="position-absolute" src="/fable/img/image.png" alt="#">
                              </label>
                              <input class="form-control my-3" type="text" placeholder="Your E-mail *">
                              <input class="form-control" type="text" placeholder="Subject">
                          </div>
                          <!-- / usercontact -->

                          <div class="txtArea col-6">
                              <textarea class="form-control" style="height: 100%" placeholder="Your Message *"></textarea>
                          </div>
                          <!-- / form -->
                      </div>
                      
                      <div class="text-center col-12 mt-4">
                          <button class="btn bgOrange">
                              SEND MESSAGE
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
:root {
  --mainColor: #d2405d;
}
  main {

        .imgColor {
            filter: hue-rotate(
            322deg) brightness(0.9);
        }
        
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
          background-color: #d2405d ;
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
                        border: 3px solid var(--mainColor);
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
                background-color: #d2405d;
            }

            .prevSlide {
                transform: translate(0, -50%);
                background-color: #d2405d;
            }

            .slideActiveImg {
              border-bottom: 2px solid #d2405d;
            }
          }
          
      }
    /* 
        / welcomeToFable
    */

      #ourClass {
        .jumboImage {
            background-image: url("/fable/img/gallery_07-690x506.jpg");
            background-repeat: no-repeat;
            background-position: center;
            background-size: cover;
            height: 500px;

            .overlay {
                  height: 100%;
                  background-color: #00000080;
                  color: white;

                  .img span {
                        display: block;
                        width: 8rem;
                        height: 8rem;
                        line-height: 8rem;
                        margin: auto;
                        border-radius: 50%;
                        border: 1px solid white;
                  }

                  .slideBars {
                      width: 2rem;
                      height: 0.7rem;
                      border: 1px solid white;
                      margin-right: 1rem;
                  }
            }
        }
        .myContainer {
          height: 100%;

            .row {
              height: 100%;
              align-items: center;
            }
        }
        
        .classes {
            p {
              margin: 0;
            }
            .myCard {
              background-color: #56509f;
              color: white;

              .yearsCol {
                border-right: 1px solid rgba(255, 255, 255, 0.212);
              }
              
            }

            img {
                  max-width: 100%;
                  height: 100% ;
                  object-fit: cover;
              }

             button {
              color: white;
              border-radius: 0;
            }
        }

        .aboutUs {
            background-color: #f5f5f5;
            ul {
              list-style-type: none;
            }
          .icons .img{
                  width: 80px;
                  height: 80px;
                  margin: auto;
                  background-color: white;
                  border-radius: 50%;
          }
        }
      }
      /* 
          / OUR CLASS
      */

      #ourStaff {
        .jumboImage {
          background-image: url("/fable/img/gallery_01.jpg"), url("/fable/img/gallery_02.jpg"), url("/fable/img/gallery_03.jpg");
          background-repeat: no-repeat;
          background-size: contain, contain, contain, contain;
          background-position: left, center, right;
        }
        .jumboText {
            background-image: url("/fable/img/pattern.png");

              .col {
                height: 5rem;
                display: flex;
                align-items: center;
                color: white;

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

        .myCard {

              img {
                height: 80%;
                object-fit: cover;
              }

              .description {
                    display: flex;
                    flex-direction: column;
                    justify-content: end;

                  p {
                    padding: 2rem;
                    padding-bottom: 3rem;
                  }

                  .icons img {
                     width: 3rem;
                     margin-right: 0.1rem;
                  }

                  .icons {
                    padding: 0 2rem;
                  }

                  .img img{
                      margin-top: 1rem;
                      border: 2px solid var(--mainColor);
                      padding-left: 4rem;
                      border-radius: 0;
                      margin-left: -2rem;
                  }

              }
        }
      }
      /* 
          / OUR STAFF
      */

      #news {

        .jumboImage {
            background-image: url("/fable/img/gallery_07-690x506.jpg");
            background-repeat: no-repeat;
            background-size: cover;
            background-position: center;

          .overlay{
              background-color: rgba(0, 0, 0, 0.404);
              height: 100%;
              color: white;

              .img{
                  border: 1px solid white;
                  width: 80px;
                  margin: auto;
                  height: 80px;
                  line-height: 80px;
                  border-radius: 50%;

                  img {
                    width: 2rem;
                  }
              }

              .slideBars .bar {
                      width: 2rem;
                      height: 0.7rem;
                      border: 1px solid white;
                      margin-right: 1rem;
              }

          }
        }
        .myContainer {
          height: 100%;
          .row {
            height: 100%;
            align-items: center;
          }

          .myCard {
            text-align: start;
              .img {
                position: relative;

                img {
                  width: 100%;
                  height: 200px;
                  object-fit: cover;
                }

                p {
                  position: absolute;
                  bottom: 0;
                  right: 0;
                  margin: 0;
                  width: 2rem;
                  height: 2rem;
                  line-height: 2rem;
                  background-color: var(--mainColor);
                  color: white;
                }
              }

              .otherCont .col-6:first-child {
                border-right: 1px solid grey;
                padding-right: 0.2rem;
              }
          }

          button {
            color: white;
            border-radius: 0;
          }

        }
      }
      /* 
          / NEWS
      */

      #contactUs {
          .jumboImage img {
            width: 100%;
            height: 100%;
            object-fit: cover;
            object-position: bottom;
          }

          .jumboImage {
            i {
                position: absolute;
                top: 19%;
                right: 61%;
                font-size: 2.2rem;
                color: #ea4335;
            }
          }

          .userContact {
              label {
                width: 100%;

                img {
                  right: 0;
                  bottom: 0;
                  padding: 0.6rem;
                }
              }
          }

          button {
            color: white;
            border-radius: 0;
          }
      }
  }
</style>