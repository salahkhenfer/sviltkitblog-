
<script>
    import Blog1 from "../../img/blog-1.jpg"
import { t, locale, locales  } from '../../lang/i18n'
import { page  } from '$app/stores'
import config from "../../config"
import { format } from "date-fns"

let cot 
$ : cot =$locale

</script>


    <!-- Page Header Start -->
    <div class="container-fluid bg-dark p-5">
        <div class="row">
            <div class="col-12 text-center">
                <h1 class="display-4 text-white">{$t("BLOG")} </h1>
       
      
            </div>
        </div>
    </div>
    <!-- Page Header End -->

  
    <!-- Blog Start -->
    <div class="container-fluid py-6 px-5">
        <div class="row g-5">
            <!-- Blog list Start -->
            <div class="col-lg-8">
                <div class="row g-5">
                    <!-- list of blogs  -->


                  {#each $page.data.posts as i}
  {#if i.id.split("-")[i.id.split("-").length - 1]=== "ar" && cot === "ar" }
     <a  href={`/${i.id}`} class="col-xl-6 col-lg-12 col-md-6 ">
                        <div class="blog-item">
                            <div class="position-relative overflow-hidden">
                                <img class="img-fluid" src={Blog1} alt="">
                            </div>
                            <div class="bg-secondary d-flex">
                                <div class="flex-shrink-0 d-flex flex-column justify-content-center text-center bg-primary text-white px-4">
                                    <span>{i.date.split("-")[0]}</span>
                                    <h5 class="text-uppercase m-0">{format(new Date(i.date), config.dateFormat).slice(0,3)}</h5>
                                    <span>{i.date.split("-")[2].slice(0,2)}</span>
                                </div>
                                <div class="d-flex flex-column justify-content-center py-3 px-4">
                                  
                                    <a class="h4" href="">{i.title}</a>
                                </div>
                            </div>
                        </div>
                    </a>

               {/if}
                 { #if i.id.split("-")[i.id.split("-").length - 1] !== "ar" && cot !== "ar" }	

                 <a  href={`/${i.id}-ar`} class="col-xl-6 col-lg-12 col-md-6 ">
                        <div class="blog-item">
                            <div class="position-relative overflow-hidden">
                                <img class="img-fluid" src={Blog1} alt="">
                            </div>
                            <div class="bg-secondary d-flex">
                                <div class="flex-shrink-0 d-flex flex-column justify-content-center text-center bg-primary text-white px-4">
                                    <span>{i.date.split("-")[0]}</span>
                                    <h5 class="text-uppercase m-0">{i.date.split("-")[1]}</h5>
                                    <span>{i.date.split("-")[2].slice(0,2)}</span>
                                </div>
                                <div class="d-flex flex-column justify-content-center py-3 px-4">
                                  
                                    <a class="h4" href="">{i.title}</a>
                                </div>
                            </div>
                        </div>
                    </a>

               {/if}
                  {/each}
              
      
<!-- end list of blogs  -->
              
                </div>
            </div>
            <!-- Blog list End -->

            <!-- Sidebar Start -->
            <div class="col-lg-4">
                <!-- Search Form Start -->
  
                <!-- Search Form End -->

 

                <!-- Recent Post Start -->
                <div class="mb-5">
                    <h2 class="mb-4">Recent Post</h2>
                          {#each $page.data.posts as i}
  {#if i.id.split("-")[i.id.split("-").length - 1]=== "ar" && cot === "ar" }
        <div class="d-flex mb-3">
            
                        <img class="img-fluid" src={Blog1} style="width: 100px; height: 100px; object-fit: cover;" alt="">
                        <a href={`/${i.id}`} class="h5 d-flex align-items-center bg-secondary px-3 mb-0">{i.title}
                        </a>
                    </div>
                          {/if}
                    { #if i.id.split("-")[i.id.split("-").length - 1] !== "ar" && cot !== "ar" }	
     
            <div class="d-flex mb-3">
                        <img class="img-fluid" src={Blog1} style="width: 100px; height: 100px; object-fit: cover;" alt="">
                        <a href="" class="h5 d-flex align-items-center bg-secondary px-3 mb-0">{i.title}
                        </a>
                    </div>
                    {/if}

                  {/each}

                
              
                </div>
     
            </div>
            <!-- Sidebar End -->
        </div>
    </div>
    <!-- Blog End -->




    <!-- Back to Top -->
    <a href="" class="btn btn-lg btn-primary btn-lg-square rounded-circle back-to-top"><i class="bi bi-arrow-up"></i></a>

