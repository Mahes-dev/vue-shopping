<template>
  <html>
    <body>
    <div class="my-jumbotron" id="my-jumbotron">
    <nav class="navbar navbar-expand">
        <img src="/pictures/logo3.png" width="80px" height="80px" class="navbar-brand p-2"/>
        <ul class="navbar-nav">
        <li class="nav-item">
            <a class="nav-link" href="">Home</a>
        </li>
        <li class="nav-item">
            <a class="nav-link" href="">About</a>
        </li>
        <li class="nav-item">
            <a class="nav-link" href="">Shop</a>
        </li>
        </ul>
        <div class="collapse navbar-collapse">
          <ul class="nav navbar-nav ml-auto">
          <li class="nav-item mx-3 ">
              <a class="nav-link" href="" ><b-icon icon="person"></b-icon></a>
          </li>
          <li class="nav-item mx-3">
              <a class="nav-link" href=""><b-icon icon="window"></b-icon></a>
          </li>
          </ul>
        </div>
        </nav>

        <!-- banner -->
        <div>
    <b-carousel
      id="carousel-1"
      v-model="slide"
      :interval="4000"
      controls
      indicators
      background="#ababab"
      img-width="1024"
      img-height="480"
      style="text-shadow: 1px 1px 2px #333;"
      @sliding-start="onSlideStart"
      @sliding-end="onSlideEnd"
    >
      <!-- Text slides with image -->
      <b-carousel-slide img-src="https://i.picsum.photos/id/1021/2048/1206.jpg">
        <div class="container text-center" id="jumbo-text-contain">
            <h4 class="display-4 mt-5" style="font-weight: bold;">Welcome To MahesStore !</h4>
            <p class="lead">Belanja Mudah di MahesStore</p>
            <button type="button" class="btn" id="jumbotron-btn">SHOP NOW !</button>
        </div>
      </b-carousel-slide>

      <!-- Slides with custom text -->
      <b-carousel-slide img-src="https://i.picsum.photos/id/1022/6000/3376.jpg">
        <div class="container text-center" id="jumbo-text-contain">
            <h4 class="display-4 mt-5" style="font-weight: bold;">Welcome To MahesStore !</h4>
            <p class="lead">Belanja Mudah di MahesStore</p>
            <button type="button" class="btn" id="jumbotron-btn">SHOP NOW !</button>
        </div>
      </b-carousel-slide>

      <!-- Slides with image only -->
      <b-carousel-slide img-src="https://picsum.photos/id/1023/3955/2094">
        <div class="container text-center" id="jumbo-text-contain">
            <h4 class="display-4 mt-5" style="font-weight: bold;">Welcome To MahesStore !</h4>
            <p class="lead">Belanja Mudah di MahesStore</p>
            <button type="button" class="btn" id="jumbotron-btn">SHOP NOW !</button>
        </div>
      </b-carousel-slide>
    </b-carousel>
  </div>
    </div>

    <div id="category-sect">
    <h4 class="font-weight-bold pt-5 text-center"> New Hijrah For You </h4>
      <section id="tabs" class="project-tab">
        <div class="container-fluid">
            <div class="row justify-content-center">
                <div class="col-md-12">
                    <b-tabs content-class="mt-3" fill>
                    <b-tab title="Kaos Kaki" active>
                    <ul class="container mt-4">
                          <div class="row">
                        <div v-for="(kaoskaki, index) in kaoskakis" :key="index" class="my-3 mr-2 text-center">
                          <div class="product-image">
                            <img :src="/pictures/ + filename + index + filetype" class="img-responsive h-75 w-100 p-2"/>
                            </div>
                          <div class="product-details">
                            <h6 class="display-6 mt-3">{{ kaoskaki.name }}</h6>
                            <h6 class="display-6 text-muted">Rp.{{ kaoskaki.price }}</h6>
                          </div>
                        </div>
                    </div>
                    </ul>
                    </b-tab>
                    <b-tab title="Kanik">
                      <ul class="container mt-4">
                          <div class="row">
                        <div v-for="(kanik, index) in kaniks" :key="index" class="my-3 mr-2 text-center">
                          <div class="product-image">
                            <img :src="/pictures/ + filejeneng + index + filetype" class="img-responsive h-75 w-100 p-2"/>
                            </div>
                          <div class="product-details">
                            <h6 class="display-6 mt-3">{{ kanik.name }}</h6>
                            <h6 class="display-6 text-muted">Rp.{{ kanik.price }}</h6>
                          </div>
                        </div>
                    </div>
                    </ul>
                      </b-tab>
                    <b-tab title="Masker">
                      <ul class="container mt-4">
                          <div class="row">
                        <div v-for="(masker, index) in maskers" :key="index" class="my-3 mr-2 text-center">
                          <div class="product-image">
                            <img :src="/pictures/ + filenama + index + filetype" class="img-responsive h-75 w-100 p-2"/>
                            </div>
                          <div class="product-details">
                            <h6 class="display-6 mt-3">{{ masker.name }}</h6>
                            <h6 class="display-6 text-muted">Rp.{{ masker.price }}</h6>
                          </div>
                        </div>
                    </div>
                    </ul>
                    </b-tab>
                  </b-tabs>

                    </div>
                </div>
            </div>
            </section>
        </div>
		
  </body>

  <footer class="page-footer blue pt-5 mt-5">
<div class="container-fluid text-center text-md-left">
      <div class="row">
        <div class="col-md-5 mt-md-0 mt-3">
          <img class="px-5" src="/pictures/logo3.png" width="180px" height="100px" />
        

        </div>

        <hr class="clearfix w-100 d-md-none pb-3">
        <div class="col-md-3 mb-md-0 mb-3">

          <h5 class="text-uppercase">Layanan Kami</h5>

          <ul class="list-unstyled">
            <li>
              <a href="Facebook">Facebook</a>
            </li>
            <li>
              <a href="#!">Instagram</a>
            </li>
            <li>
              <a href="#!">Twitter</a>
            </li>
           
          </ul>

        </div>
        <div class="col-md-3 mb-md-0 mb-3">

          <h5 class="text-uppercase">TENTANG KAMI</h5>

          <ul class="list-unstyled">
            <li>
              <a href="#!">Prestasi</a>
            </li>
            <li>
              <a href="#!">Partner Ship</a>
            </li>
            <li>
              <a href="#!">Rekor</a>
            </li>
           
          </ul>

        </div>

      </div>

    </div>

    <div class="footer-copyright text-center py-3 mr-3">© 2020 Copyright: MahesStore
    </div>
  </footer>

  </html>
</template>

<script>
import axios from 'axios'
import 'bootstrap/dist/css/bootstrap.css'
import 'bootstrap-vue/dist/bootstrap-vue.css'

export default {
    data() {
      return {
        slide: 0,
        filetype:".jpeg",
        filename:"kaoskaki",
        filejeneng:"kanik",
        filenama:"masker",
        sliding: null,
        kaoskakis: [],
        kaniks: [],
        maskers: []
      }
    },
  async created () {
    const baseURI = 'https://my-json-server.typicode.com/Mahes-dev/vuee/db'
    axios.get(baseURI)
      .then((result) => {
        this.kaoskakis = result.data.kaoskakis
        this.kaniks = result.data.kaniks
        this.maskers = result.data.maskers
      })
  }
  }
</script>

<style>
.navbar {
background: white;
}
#my-jumbotron {
    background-size: cover;
    overflow: hidden;
}
#jumbo-text-contain {
    color: white;
    min-height: 440px;
}
#jumbotron-btn {
    font-size: 20px;
    border: 3px solid ;
    border-radius: 0;
    transition: 0.3s;
    color: white;
}
#jumbotron-btn:hover {
    color:white ;
    border: 1px solid white;
}
#products-container li{
    list-style-type: none;
    height: 250px;
}
.product-image {
    background: #f4f4ef;
    width: 250px;
    height: 250px;
    transition: 0.5s ease-in-out;
}
.product-image:hover {
  box-shadow: 1px 4px 8px 1px rgba(0, 0, 0, 2);
}
.project-tab {
    padding: 10%;
    margin-top: -8%;
}
.project-tab #tabs{
    background: black;
    color: #eee;
}
.project-tab #tabs h6.section-title{
    color: #eee;
}
.project-tab #tabs .nav-tabs .nav-item.show .nav-link, .nav-tabs .nav-link.active {
    color: #20232a;
    background-color: transparent;
    border-color: transparent transparent #f3f3f3;
    border-bottom: 3px solid !important;
    font-size: 16px;
    font-weight: bold;
}
.project-tab .nav-link {
    border: 1px solid transparent;
    border-top-left-radius: .25rem;
    border-top-right-radius: .25rem;
    color: #acbebe;
    font-size: 16px;
    font-weight: 600;
}
.project-tab .nav-link:hover {
    border: none;
}
.project-tab thead{
    background: #f3f3f3;
    color: #333;
}
.project-tab a{
    text-decoration: none;
    color: #333;
    font-weight: 600;
}
.page-footer {
    color: white;
    background: gray;
}
</style>
