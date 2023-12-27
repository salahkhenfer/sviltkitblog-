<script>
import { t, locale, locales  } from '../lang/i18n'

import "../css/style.css"
import "../css/bootstrap.min.css"

import featurelImg from "../img/feature.jpg"
import quoteImg from "../img/quote.jpg"
import blogImg from "../img/blog-1.jpg"
import blogImg2 from "../img/blog-2.jpg"
import blogImg3 from "../img/blog-3.jpg"

import Service from '../pages/Service.svelte'
import Team from '../pages/Team.svelte'
import Testimonial from '../pages/Testimonial.svelte'
import Carousel from "../pages/Carousel.svelte"
import About from "../pages/About.svelte"
import UseCases from "../pages/UseCases.svelte"
import { format } from 'date-fns'
import config from '../config'
import { page } from '$app/stores'


let cot 
$ : cot =$locale
</script>
 


    <!-- Carousel Start -->
<Carousel/>
    <!-- Carousel End -->


    <!-- About Start -->
<About/>
    <!-- About End -->
    

    <!-- Services Start -->
  <Service/>
    <!-- Services End -->


    <!-- Features Start -->
    <!-- <div class="container-fluid py-6 px-5">
        <div class="text-center mx-auto mb-5" style="max-width: 600px;">
            <h1 class="display-5 mb-0">Why Choose Us!!!</h1>
            <hr class="w-25 mx-auto bg-primary">
        </div>
        <div class="row g-5">
            <div class="col-lg-4">
                <div class="row g-5">
                    <div class="col-12">
                        <div class="bg-primary rounded-circle d-flex align-items-center justify-content-center mb-3" style="width: 60px; height: 60px;">
                            <i class="fa fa-cubes fs-4 text-white"></i>
                        </div>
                        <h3>Best In Industry</h3>
                        <p class="mb-0">Magna sea eos sit dolor, ipsum amet ipsum lorem diam dolor eos diam et diam dolor ea</p>
                    </div>
                    <div class="col-12">
                        <div class="bg-primary rounded-circle d-flex align-items-center justify-content-center mb-3" style="width: 60px; height: 60px;">
                            <i class="fa fa-percent fs-4 text-white"></i>
                        </div>
                        <h3>99% Success Rate</h3>
                        <p class="mb-0">Magna sea eos sit dolor, ipsum amet ipsum lorem diam dolor eos diam et diam dolor ea</p>
                    </div>
                    <div class="col-12">
                        <div class="bg-primary rounded-circle d-flex align-items-center justify-content-center mb-3" style="width: 60px; height: 60px;">
                            <i class="fa fa-award fs-4 text-white"></i>
                        </div>
                        <h3>Award Winning</h3>
                        <p class="mb-0">Magna sea eos sit dolor, ipsum amet ipsum lorem diam dolor eos diam et diam dolor ea</p>
                    </div>
                </div>
            </div>
            <div class="col-lg-4">
                <div class="d-block bg-primary h-100 text-center">
                    <img class="img-fluid" src={featurelImg} alt="">
                    <div class="p-4">
                        <p class="text-white mb-4">Clita nonumy sanctus nonumy et clita tempor, et sea amet ut et sadipscing rebum amet takimata amet, sed accusam eos eos dolores dolore et. Et ea ea dolor rebum invidunt clita eos. Sea accusam stet stet ipsum, sit ipsum et ipsum kasd</p>
                        <a href="" class="btn btn-light py-md-3 px-md-5 rounded-pill mb-2">Learn More</a>
                    </div>
                </div>
            </div>
            <div class="col-lg-4">
                <div class="row g-5">
                    <div class="col-12">
                        <div class="bg-primary rounded-circle d-flex align-items-center justify-content-center mb-3" style="width: 60px; height: 60px;">
                            <i class="far fa-smile-beam fs-4 text-white"></i>
                        </div>
                        <h3>100% Happy Client</h3>
                        <p class="mb-0">Magna sea eos sit dolor, ipsum amet ipsum lorem diam dolor eos diam et diam dolor ea</p>
                    </div>
                    <div class="col-12">
                        <div class="bg-primary rounded-circle d-flex align-items-center justify-content-center mb-3" style="width: 60px; height: 60px;">
                            <i class="fa fa-user-tie fs-4 text-white"></i>
                        </div>
                        <h3>Professional Advisors</h3>
                        <p class="mb-0">Magna sea eos sit dolor, ipsum amet ipsum lorem diam dolor eos diam et diam dolor ea</p>
                    </div>
                    <div class="col-12">
                        <div class="bg-primary rounded-circle d-flex align-items-center justify-content-center mb-3" style="width: 60px; height: 60px;">
                            <i class="fa fa-headset fs-4 text-white"></i>
                        </div>
                        <h3>24/7 Customer Support</h3>
                        <p class="mb-0">Magna sea eos sit dolor, ipsum amet ipsum lorem diam dolor eos diam et diam dolor ea</p>
                    </div>
                </div>
            </div>
        </div>
    </div> -->
    <!-- Features Start -->




    <!-- Team Start -->
<!-- <Team/> -->
    <!-- Team End -->


    <!-- Testimonial Start -->
 <Testimonial/>
    <!-- Testimonial End -->

    <!-- UseCases start  -->
    <UseCases/>
    <!-- UseCases end  -->

    <!-- Blog Start -->
    <div class="container-fluid py-6 px-5">
        <div class="text-center mx-auto mb-5" style="max-width: 600px;">
            <h1 class="display-5 mb-0">{$t("LatestBlogPost")}</h1>
            <hr class="w-25 mx-auto bg-primary">
        </div>

        <div class="row g-5">
       {#each  $page.data.posts.slice(0, 4)  as i }
     
    {#if i.id.split("-")[i.id.split("-").length - 1]=== "ar" && cot === "ar" }
    <div class="col-lg-4">
   <a href={`${i.id}`}>
                <div class="blog-item">
                    <div class="position-relative overflow-hidden">
                        <img class="img-fluid" src={blogImg} alt="">
                    </div>
                    <div class="bg-secondary d-flex">
                     <div class="flex-shrink-0 d-flex flex-column justify-content-center text-center bg-primary text-white px-4">
                                    <span>{i.date.split("-")[0]}</span>
                                    <h5 class="text-uppercase m-0">{format(new Date(i.date), config.dateFormat).slice(0,3)}</h5>
                                    <span>{i.date.split("-")[2].slice(0,2)}</span>
                                </div>
                        <div class="d-flex flex-column justify-content-center py-3 px-4">
                            <div class="d-flex mb-2">
                                <small class="text-uppercase me-3"><i class="bi bi-person me-2"></i>Admin</small>
                                <small class="text-uppercase me-3"><i class="bi bi-bookmarks me-2"></i>Web Design</small>
                            </div>
                            <a class="h4" href="">{i.title}</a>
                        </div>
                    </div>
                </div>
            </a>
        </div>
  
         

               {/if}
                 { #if i.id.split("-")[i.id.split("-").length - 1] !== "ar" && cot !== "ar" }	
                 <div class="col-lg-4">
   <a href={`${i.id}`}>
                <div class="blog-item">
                    <div class="position-relative overflow-hidden">
                        <img class="img-fluid" src={blogImg} alt="">
                    </div>
                    <div class="bg-secondary d-flex">
                     <div class="flex-shrink-0 d-flex flex-column justify-content-center text-center bg-primary text-white px-4">
                                    <span>{i.date.split("-")[0]}</span>
                                    <h5 class="text-uppercase m-0">{format(new Date(i.date), config.dateFormat).slice(0,3)}</h5>
                                    <span>{i.date.split("-")[2].slice(0,2)}</span>
                                </div>
                        <div class="d-flex flex-column justify-content-center py-3 px-4">
                            <div class="d-flex mb-2">
                                <small class="text-uppercase me-3"><i class="bi bi-person me-2"></i>Admin</small>
                                <small class="text-uppercase me-3"><i class="bi bi-bookmarks me-2"></i>Web Design</small>
                            </div>
                            <a class="h4" href="">{i.title}</a>
                        </div>
                    </div>
                </div>
            </a>
        </div>
         

               {/if}
                  {/each}

        
        </div>
    </div>

          
    <!-- Blog End -->
    



    <!-- Back to Top -->
    <a href="" class="btn btn-lg btn-primary btn-lg-square rounded-circle back-to-top"><i class="bi bi-arrow-up"></i></a>


       
