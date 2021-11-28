<template>
  <main>
    <section id="welcomeToFable">
        <div class="jumboImage position-relative">
          <img v-if="active == 0" class="trenino" :src="bgs1[active]" alt="#">
          <img v-else :src="bgs1[active]" class="bgJumboFable" alt="#">
          <img v-show="active == 0" class="lego" src="/fable/img/slider_slide3_img3.png" alt="#">
          <!--  -->
          <div class="slideBars">
              <div @click="changeBg(index)" class="bar" :class="(active == index && index > 0) ? 'activeBar white' : active == index ? 'activeBar' : ''"
              v-for="(toy, index) in bgs1" :key="index"></div>
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
                    <button class="btn purpleBtn">
                        learn more <img style="width: 2rem" src="/fable/img/slider_next.png" alt="#">
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
                      <button @click="show = true" class="btn mb-4" :class="{bgOrange: show, unactive: !show}">
                          Overview
                      </button>
                      <button @click="show = false" class="btn mb-4" :class="{bgOrange: !show, unactive: show}">
                          Our Mission
                      </button>
                      <!--
                         / buttons 
                      -->
                      <!-- / overview title -->
                      <div v-if="show == true" class="overviewCont">
                          <p class="title fs-4 mb-4">
                          Lorem ipsum dolor sit amet consectetur adipisicing elit. Neque, officia?
                          </p>
                          <div v-for="index in 2" :key="index" class="description d-flex mb-3">

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
                      </div>
                          <!--  -->

                       <div v-else class="overviewCont">
                          <p class="title fs-4 mb-4">
                              Other title Lorem, ipsum dolor.
                          </p>
                          <div v-for="index in 2" :key="index" class="description d-flex mb-3">

                              <div class="me-3">
                                <div class="img rounded-circle bgOrange">
                                    <img src="/fable/img/diagram_alt.png" alt="#">
                                </div>
                              </div>
                              
                              <div class="txt">
                                  <p class="title fs-5 mb-1">
                                      Something Else
                                  </p>
                                  <p class="fs-6 descr">
                                      Something Else
                                  </p>
                              </div>
                          </div>
                      </div>


                    <!-- / DESCRIPTION -->
                  </div>
                  <!-- 
                    / txt e overview
                   -->
                  <div class="col-6">
                    <div class="row g-2">

                          <div class="slideImages col-12 position-relative"> 
                              <img class="img" :src="slideImgs[active]" alt="#">   
                              <img  @click="nextSlide()" class="nextSlide position-absolute top-50 end-0 slideIconHover" src="/fable/img/slider_next.png" alt="#">
                              <img @click="prevSlide()" class="prevSlide position-absolute top-50 start-0 slideIconHover" src="/fable/img/slider_previous.png" alt="#">
                          </div>
                      
                          <div v-for="(img, index) in slideImgs " :key="index" class="col-4 pb-2">
                            <img class="img-fluid pb-2" :class="index == active ? 'slideActiveImg' : ''" :src="img" alt="#">
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

      <div class="jumboImage" :style="`background-image: url(${ourclassBgs[active2]})`">
        <div class="overlay">
          <div class="myContainer">
              <div class="row">
                <!-- cerchi -->
                  <div v-for="(circle, index) in ourclassCircle" :key="index" class="col-3 text-center">
                      <div class="img imgColor mb-2">
                          <span class="fs-1 fw-light">
                              {{circle.num}}
                          </span>
                      </div>

                      <div class="txt">
                          <p class="fs-4">
                              {{circle.title}}
                          </p>
                          <p class="fs-6">
                              Lorem ipsum dolor sit, amet consectetur adipisicing elit.
                          </p>
                      </div>
                  </div>
                  <!-- / cerchio -->
                  <div class="col-12 d-flex justify-content-center">
                      <div @click="active2 = index" v-for="(img, index) in ourclassBgs" :key="index" 
                      class="slideBars" :class="index == active2 ? 'activeBar' : ''">
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
                      <div v-for="(card, index) in ourClassCards" :key="index" class="col-6 d-flex">
                          <div class="myCard col-6 d-flex flex-wrap ">
                              <div class="pt-3 ps-3 col-12 mb-5">
                                  <p class="fs-4">
                                     {{card.title}}
                                  </p>
                                  <p class="fs-6 fw-light">
                                    Class Name
                                  </p>
                              </div>
                              <!-- / title -->

                              <div class=" yearsCol col-6 mb-2 text-center">
                                  <p class="fs-5">
                                     {{card.numbers}}
                                  </p>
                                  <p class="fs-6 fw-light">
                                      {{card.monthYears}}
                                  </p>
                              </div>
                              <!-- / years -->

                              <div class="col-6 mb-2 text-center ">
                                 <p class="fs-5">
                                     {{card.classSize}}
                                  </p>
                                  <p class="fs-6 fw-light">
                                      Class size
                                  </p>
                              </div>
                              <!-- / class size -->
                          </div>

                          <div class="col-6 position-relative">
                              <img :src="card.img" alt="#">
                              <button class="btn position-absolute bottom-0 end-0 bgOrange d-flex align-items-center normalBtn">
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
                        <div class="col-6 text-center mb-3" v-for="(card,index) in aboutUsimgs" :key="index">
                              <div class="img imgColor mb-3 position-relative">
                                <img class="position-absolute top-50 start-50 translate-middle" :src="card.img" alt="#">
                              </div>
                              <p class="title fs-5 fw-normal">
                                  {{card.title}}
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
                        <button class="btn purpleBtn">
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
                        <h2 class="fs-1 fw-light title">
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
                    <div v-for="(teacher, index) in teachers" :key="index" class="myCard col-6 d-flex">
                        <div class="col-6 text-center">
                            <img class="teacherImg img-fluid" :src="teacher.img" alt="#">
                            <p class="fs-5 title m-0 mt-3">
                                {{teacher.name}}
                            </p>
                            <p class="fs-6 descr">
                                {{teacher.job}}
                            </p>
                        </div>
                        <!-- /teacher name -->

                        <div class="col-6 description">
                            <div class="img">
                                <img class="imgColor btn" src="/fable/img/quote.png" alt="#">
                            </div>
                            <p class="fs-6 descr">
                                {{teacher.descr}}
                            </p>
                            <div class="icons">
                                <img v-for="icon in teacher.icons" :key="icon" class="bgOrange" :src="icon" alt="#">
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
                    <div v-for="( card, index) in newsCard" :key="index" class="myCard col-4">
                        <p class="fs-6 descr">
                            {{card.date}}
                        </p>
                        <div class="img">
                            <img :src="card.img" alt="#">
                            <p>
                                {{card.number}}
                            </p>
                        </div>
                        <!-- / img -->

                        <p class="fs-5 title mt-3">
                            {{card.title}}
                        </p>

                        <p class="fs-6 descr">
                            Lorem ipsum dolor sit amet consectetur adipisicing elit. Numquam quam quos similique fugiat, nisi nemo. Vitae, nemo vero. Id corrupti a assumenda eos impedit, consequatur magnam saepe? Quas, qui laudantium.
                        </p>
                        <hr>

                        <!-- / description -->

                        <div class="otherCont d-flex">
                            <div class="col-6">
                                <p class="fs-6 descr">
                                  <img class="imgColor" src="/fable/img/author.png" alt="#">
                                  Anna Brown
                                </p>
                            </div>

                            <div class="col-6">
                                <p class="fs-6 descr ps-3">
                                    <img class="imgColor" src="/fable/img/category.png" alt="#">
                                    {{card.events}}
                                </p>
                            </div>
                        </div>

                    </div>
                    <!-- / card-->


                    <div class="col-12 pt-5">
                        <button class="btn bgOrange normalBtn">
                            GO TO BLOG 
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
                          <h2 class="fs-1 fw-light title">
                            Contact Us
                          </h2>
                          <p class="fs-6 descr">
                              Lorem ipsum dolor sit.
                          </p>
                          <img class="imgColor" src="/fable/img/header_divider.png" alt="#">
                      </div>
                      <!-- / title -->

                      <!-- card -->
                      <div class="col-3 myCard" v-for="(card, index) in contactUsCards" :key="index"> 
                            <div class="text-center mb-3">
                                <div class="img mb-3 ">
                                  <img class="imgColor" :src="card.img" alt="#">
                                </div>
                                <p class="title fs-5 fw-normal">
                                    {{card.title}}
                                </p>
                                <p class="fs-6 descr">
                                    {{card.descr}}
                                    <a href="#"> {{card.mail}} </a>
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
                          <button class="btn bgOrange normalBtn">
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
      simpleCard,
    },

    data() {
      return {
          show: true,

          /* jumbo slides welcome */
            bgs1: [
              '/fable/img/slider_slide3_img2.png',
              'https://www.ioamofirenze.it/wp-content/uploads/2013/09/smilinghand.jpg',
              'https://www.pngitem.com/pimgs/m/74-743340_kids-hands-png-child-development-transparent-png.png'
            ],
          /* / jumbo slides welcome */

          /* jumbo slide in our class */
          ourclassBgs: [
            '/fable/img/gallery_07-690x506.jpg',
            'https://www.sheknows.com/wp-content/uploads/2018/08/preschoolers-600_rnnjrt.jpeg',
            'https://www.westend61.de/images/0000035341pw/children-4-7-in-class-room-holding-school-cones-WESTF04571.jpg',
            'https://www.rd.com/wp-content/uploads/2016/04/33-your-childs-teacher-happy-kids-classroom.jpg',
            'https://st3.depositphotos.com/1394201/i/600/depositphotos_348225444-stock-photo-nursery-children-playing-with-teacher.jpg',
            'https://thumbs.dreamstime.com/b/children-kids-diversity-friendship-happiness-cheerful-concept-56679027.jpg',
          ],

          ourclassCircle: [
            {
              num: 507,
              title: 'Our Pupils',
            },
            {
              num: 235,
              title: 'Teaching Hours',
            },
            {
              num: '100%',
              title: 'Satisfied Parents',
            },
            {
              num: 1050,
              title: 'Meals per Year',
            },
          ],
          /* / jumbo slide in our class */

          /* whats new jumbo slides */

          /* / whats new jumbo slides */

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

          slideImgs: [
            '/fable/img/gallery_07-690x506.jpg',
            '/fable/img/gallery_01-690x506.jpg',
            '/fable/img/gallery_08-690x506.jpg',
          ],

          active: 0,
          active2: 0,

          /* 
              OUR CLASS
          */

          ourClassCards: [
            {
              title: 'Little Lambs',
              img: '/fable/img/gallery_04.jpg',
              numbers: '12-24',
              monthYears: 'Month Old',
              classSize: '9'
            },
            {
              title: 'Bouncy Bears',
              img: '/fable/img/class_02-690x506.jpg',
              numbers: '2-3',
              monthYears: 'Year old',
              classSize: '12'
            },
            {
              title: 'TenderHearts',
              img: '/fable/img/class_03-690x506.jpg',
              numbers: '3-4',
              monthYears: 'Year olds',
              classSize: '15'
            },
            {
              title: 'Shining Stars',
              img: '/fable/img/class_04-690x506.jpg',
              numbers: '4-5',
              monthYears: 'Year olds',
              classSize: '20'
            }
          ],

          aboutUsimgs: [
            {
              title: 'Learning & Fun',
              img: '/fable/img/toy.png',
            },
            {
              title: 'Healthy Meals',
              img: '/fable/img/meal.png',
            },
            {
              title: 'Friendly Place',
              img: '/fable/img/school.png',
            },
            {
              title: 'Children Safety',
              img: '/fable/img/shield.png',
            },
          ],

          /* 
              OUR STAFF
          */

         teachers: [
           {
             name: 'Ruth Richie',
             job: 'Teacher',
             descr: 'I have just finished my studies in Early Childhood education, and i am also the kids yoga teacher here at Fable. I enjoy     cooking, swimming and bike riding in my free time',
             icons: [
               '/fable/img/mail.png',
               '/fable/img/facebook.png',
               '/fable/img/pinterest.png',
             ],
             img: '/fable/img/gallery_08-690x506.jpg'
           },
           {
             name: 'Katie Willmore',
             job: 'Assistant Teacher',
             descr: 'My name is Katie, i grew up and studied in Canada, this is my second year at Fable and love every minute of it, making the childrens learning experience fun.',
             icons: [
               '/fable/img/dribbble.png',
               '/fable/img/stumbleupon.png',
               '/fable/img/instagram.png',
             ],
             img: '/fable/img/team_03.jpg'
           },
           {
             name: 'Angelica Watson',
             job: 'Lead Teacher',
             descr: 'I hold a degree in Early Child education and an advanced English language certificate. i have been working as a kindergarten teacher since 2002',
             icons: [
               '/fable/img/bing.png',
               '/fable/img/skype.png',
               '/fable/img/linkedin.png',
             ],
             img: '/fable/img/team_02.jpg'
           },
           {
             name: 'Angela Lynn ',
             job: 'Teacher',
             descr: 'I have complete a graduate diploma in Early Childhood teaching. I have worked with children aged from six weeks to eight years. this is my second year at Fable',
             icons: [
               '/fable/img/youtube.png',
               '/fable/img/twitter.png',
               '/fable/img/googleplus.png',
             ],
             img: '/fable/img/team_01.jpg'
           }
         ],

         /* 
            WHAT'S NEW CARDS
         */

          newsCard: [
            {
              date: 'October 03, 2014',
              img: '/fable/img/gallery_03.jpg',
              title:  'Drawing and Painting Lessons',
              events: 'Events, Fun',
              number: 42,
            },
            {
              date: 'October 03, 2014',
              img: '/fable/img/class_04-690x506.jpg',
              title:  'Fall Parents Meeting Day',
              events: 'Dance, Education',
              number: 19,
            },
            {
              date: 'September 20, 2014',
              img: '/fable/img/blog_08-525x315.jpg',
              title:  'Birthday in Kindergarten',
              events: 'Games, General',
              number: 22,
            },
          ],

          /* 
            contact us cards
          */

         contactUsCards: [
           {
             title: 'Postal Address',
             img: '/fable/img/envelope (1).png',
             descr: `Fable Care Center 
                      85 Fentiman Ave 
                      Ottawa, ON K1S OT7`,
            mail: '',
           },
           {
             title: 'Phone & E-mail',
             img: '/fable/img/mobile.png',
             descr: `Phone: 1-800-64-38 
                      Fax: 1-800-64-39 
                     `,
            mail: 'office@fable.com',
           },
           {
             title: 'Business Hours',
             img: '/fable/img/clock.png',
             descr: `Monday - Friday 
                      8.00 am - 5.00 pm 
                      Weekend Closed`,
            mail: '',
           },
           {
             title: 'Sessions',
             img: '/fable/img/document (1).png',
             descr: `Mornings, 8 am - 12 noon
                      Afternoons, 1 pm - 5 pm
                      Full Day, 8 am - 5 pm`,
            mail: '',
           },
         ]
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
      }, 
      prevSlide() {
          
          if(this.active == 0) {
              this.active = this.slideImgs.length - 1; 
          }
          else {
            this.active--
          }
      },
      
      nextSlide() {
            this.active++          
           if(this.active == this.slideImgs.length) {
              this.active = 0; 
          }
      },
    changeBg(index) {
        this.active = index;
      },
    },
  }
</script>

<style lang="scss">
button:focus {
  box-shadow: 2px 2px 2px #9c253d!important;
}
.bgJumboFable {
    width: 100%;
    height: 100%;
    object-fit: cover;
    object-position: center;
}
.purpleBtn {
                      &:hover {
                        background-color: white;
                        color: var(--titleColor)!important;
                      }
                      &:hover img {
                            filter: brightness(0.7) hue-rotate(
                            234deg) saturate(9) contrast(0.5);
                      }
            }

  .normalBtn {
     &:hover {
      background-color: white;
      color: var(--titleColor)!important;
      border: 1px solid var(--titleColor);
    }
    &:hover img {
          filter: brightness(0.7) hue-rotate(
          234deg) saturate(9) contrast(0.5);
    }
  } 

  .slideIconHover {
      &:hover {
        border: 1px solid white;
      }
  }

  .activeBar {
      position: relative;
      bottom: 1rem;
      &.white {
        border: 2px solid white!important;
      }
  }



  main {

       
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
                    bottom: 4rem;
                    left: 50%;
                    transform: translate(-50%, 0);
                    width: 200px;
                    height: 100px;
                    object-fit: contain;
              }

              .lego {
                position: absolute;
                left: 80%;
                bottom: 3rem;
                 width: 100px;
                height: 100px;
                object-fit: contain;
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

                      &:hover {
                        background-color: white;
                        color: var(--titleColor);
                      }
                      &:hover img {
                            filter: brightness(0.7) hue-rotate(
                            234deg) saturate(9) contrast(0.5);
                      }
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
                cursor: pointer;
            }

            .prevSlide {
                transform: translate(0, -50%);
                background-color: #d2405d;
                cursor: pointer;
            }

            .slideImages {
              .img {
                height: 100%;
                width: 100%;
                object-fit: cover;
                object-position: center;
              }

            }

            .slideActiveImg {
              border-bottom: 2px solid #d2405d;
              animation-name: border-fade;
              animation-duration: 1.5s;

              @keyframes border-fade {
                from {
                  border-bottom: 2px solid rgba(255, 255, 255, 0);
                }
                to {border-bottom: 2px solid #d2405d;}
              }
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
                  background-color: #0000003d;
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
              
              transition: 0.5s;

              &:hover {
                background-color: #f5f5f5;
                padding-left: 0;
                box-shadow: 2px 2px 5px grey;
                border-radius: 1rem;
              }

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
                  text-align: center;
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