<script>

import { t, locale, locales } from '../lang/i18n'
import "../css/index.css"
import "../css/style.css"
import "../css/bootstrap.min.css"
import App from "../lang/App.svelte"
import Header from '../pages/Header.svelte'
import UseCases from '../pages/UseCases.svelte'

    


    let cot 
$ : cot =$locale


</script>

 
 <!-- Header Start -->
<Header/>
     <!-- Header end -->

 <slot />
    <!-- Footer Start -->


    <div class={`container-fluid bg-dark  d-flex text-secondary  justify-content-around align-items-center text-center border-top py-4 px-5" style="border-color: rgba(256, 256, 256, .1) !important ; ${cot == "ar" && "durationRtl" } `}>
                 
 <p class="m-0 ">&copy; {$t("AllRightsReserved")} </p>
      <div class="d-flex text-align-center justify-content-center ">
                    <a class="btn btn-lg btn-primary btn-lg-square rounded-circle me-2 d-flex justify-content-center align-items-center" href="#"><i class="fab fa-twitter fw-normal"></i></a>
                    <a class="btn btn-lg btn-primary btn-lg-square rounded-circle me-2  d-flex justify-content-center align-items-center" href="#"><i class="fab fa-facebook-f fw-normal "></i></a>
                    <a class="btn btn-lg btn-primary btn-lg-square rounded-circle me-2 d-flex justify-content-center align-items-center" href="#"><i class="fab fa-linkedin-in fw-normal "></i></a>
                    <a class="btn btn-lg btn-primary btn-lg-square rounded-circle me-2 d-flex justify-content-center align-items-center" href="#"><i class="fab fa-instagram fw-normal "></i></a>
                </div>
</div>
    <!-- Footer End -->


