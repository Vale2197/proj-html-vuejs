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
                             <a href="#"> MONTH (YEAR) </a> 
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
                      
                      <div v-for="(card, index) in footerCard" :key="index" class="cardFooter col-12 d-flex align-items-center">
                          <div class="col-6">
                              <img class="img" :src="card.img" alt="#">
                          </div>
                          <div class="col-6 p-2">
                              <p class="fs-5">
                                  {{card.title}}
                              </p>

                              <p class="fs-6 fw-light">
                                  <img class="me-2" src="/fable/img/date_footer.png" alt="#">
                                  {{card.date}}
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
                 <img v-for="(icon, index) in footerIcons" :key="index" class="bgOrange me-1" :src="icon" alt="#">
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
    data() {
      return {
        footerCard: [
          {
            img: '/fable/img/gallery_03.jpg',
            title: 'Drawing and Painting Lessons',
            date: 'October 03, 2014',
          },
          {
            img: '/fable/img/blog_10-300x180.jpg',
            title: 'Fall Parents and Meeting Day',
            date: 'October 03, 2014',
          },
          {
            img: '/fable/img/blog_08-300x180.jpg',
            title: 'Birthday in Kindergarten',
            date: 'September 20, 2014',
          },
        ],

        footerIcons: [
          '/fable/img/behance.png',
          '/fable/img/dribbble.png',
          '/fable/img/envato.png',
          '/fable/img/facebook.png',
          '/fable/img/twitter.png',
        ]
      }
    }
}
</script>

<style lang="scss">
  footer {
    a {
      text-decoration: none;
      color: white;
      transition: 0.2s;

      &:hover {
        font-weight: bold;
        color: white;
      }
    }
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

        .cardFooter .img {
          width: 120px;
          height: 120px;
          object-fit: cover;
        }

        .cardFooter{
          cursor: pointer;
          transition: 0.3s;

          &:hover {
            border-bottom: 2px solid white;
            margin-bottom: 0.2rem;
            padding-bottom: 0.2rem;
          }
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