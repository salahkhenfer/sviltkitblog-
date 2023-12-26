<script>
import testimonialImg from "../img/testimonial.jpg"
    import { t, locale, locales } from '../lang/i18n'
    let cot 
$ : cot =$locale

</script>
    <!-- Testimonial Start -->
    <div  class={ ` container-fluid bg-secondary p-0 ${cot == "ar" && "durationRtl" } `}>
        <div class={ ` row g-0 container-fluid bg-secondary p-0  `}>
            <div class="col-lg-6" style="min-height: 500px;">
                <div class="position-relative h-100">
                    <img class=" w-100 h-100" src={testimonialImg} style="object-fit: cover;">
                </div>
            </div>
            <div class={`col-lg-6 py-6 px-5 ${cot == "ar" && "" } `}>
                <h1 class={`display-5 text-center ${cot == "ar" && "durationRtl" }  mb-5 `}>{$t("OurClient")}</h1>
                <div class="owl-carousel testimonial-carousel">
{#each $t("Testimonials") as element}
                 
                     <div  class={` testimonial-item ${cot == "ar" && "durationRtl" } `}>
                        <div class="fs-4 fw-normal   text-center "> <i class= {` fa ${cot == "en" ? "fa-quote-left" :"fa-quote-right" } text-primary`}></i>{element.testimonial}</div>
                        <div class="   ">
                            <div class="ps-4 mb-5 ">
                                <h3 class="text-center">{element.client}</h3>
                        
                            </div>
                        </div>
                    </div>
                    
{/each}
                  
           
                </div>
            </div>
        </div>
    </div>
    <!-- Testimonial End -->