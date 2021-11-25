<template>
  <header>
      <div class="myContainer">

          <div class="row align-items-stretch">
              <div class="logo col">
                  <img src="../assets/fable/img/logo.png" alt="FableLogo">
              </div>
              <!-- / logo -->
              <div class="navBar col">
                  <ul class="navItems d-flex">
                        <li>
                            <img src="../assets/fable/home.png" alt="#">
                            <a href="#"> Home </a>
                        </li> 

                        <li>
                            <img src="../assets/fable/document.png" alt="#">
                            <a href="#"> Pages </a>
                        </li>

                        <li>
                            <img src="../assets/fable/printer.png" alt="#">
                            <a href="#"> Blog </a>
                        </li>

                        <li>
                            <img src="../assets/fable/cart.png" alt="#">
                            <a href="#"> Shop </a>
                        </li>

                        <li>
                            <img src="../assets/fable/lab.png" alt="#">
                            <a href="#"> ShortCodes </a>
                        </li>

                        <li>
                            <img src="../assets/fable/chat.png" alt="#">
                            <a href="#"> Support </a>
                        </li>

                        <li>
                            <img src="../assets/fable/envelope.png" alt="#">
                            <a href="#"> Contact </a>
                        </li>   
                  </ul>
              </div>
              <!-- / nav -->
          </div>
          <!-- / row -->

      </div>
  </header>
</template>

<script>

export default {
    data() {
        return {
            
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
                        background-color: #fd6500;
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