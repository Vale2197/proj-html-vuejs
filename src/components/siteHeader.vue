<template>
  <header>
      <div class="myContainer">

          <div class="row align-items-stretch">
              <div class="logo col">
                  <img src="/fable/img/logo.png" alt="FableLogo">
              </div>
              <!-- / logo -->
              <div class="navBar col">
                  <ul class="navItems d-flex">
                        <linkHeader v-for="link in headerLinks" :key="link.title" :image="link.img" :title="link.title"/>
                  </ul>
              </div>
              <!-- / nav -->
          </div>
          <!-- / row -->

      </div>
  </header>
</template>

<script>
import linkHeader from "./linkHeader.vue";

export default {
    components: {
        linkHeader
    },
    data() {
        return {
            headerLinks: [
                {
                    title: 'Home',
                    img: '/fable/home.png'
                },

                {
                    title: 'Pages',
                    img: '/fable/document.png'
                },

                {
                    title: 'Blog',
                    img: '/fable/printer.png'
                },

                {
                    title: 'Shop',
                    img: '/fable/cart.png'
                },

                {
                    title: 'Shortcodes',
                    img: '/fable/lab.png'
                },

                {
                    title: 'Support',
                    img: '/fable/chat.png'
                },

                {
                    title: 'Contact',
                    img: '/fable/envelope.png'
                }
            ]
        }
    },
}
</script>

<style lang="scss">  
    .myContainer {
        width: 70%;
        margin: auto;

        .logo img{
            height: 150px;
            width: 200px;
            object-fit: contain;
        }
    }

    header {
        /* height: 100px; */
        background-color: white; 

        .navBar {
            /* height: 100px; */

        .navItems {
            list-style-type: none;
            list-style-type: none;
            height: 100%;
            align-items: center;
                li {
                    padding: 1.5rem;
                    display: flex;
                    flex-direction: column;
                    align-items: center;
                    height: 100%;
                    justify-content: center;
                    transition: 0.3s;

                    &:hover {
                        background-color: #d2405d;
                    }

                    img {
                    display: block;
                    margin-bottom: 0.3rem;
                    } 

                    &:hover img {
                        filter: brightness(3);
                    }

                    a {
                        text-decoration: none;
                        color: grey;
                        transition: 0.3s;
                    }

                    &:hover a{
                        color: white;
                    }

                }
        }
      }
    }

</style>