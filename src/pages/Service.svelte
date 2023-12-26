<script>
    /** @type {import('./$types').PageData} */

    import quote from "../img/quote.jpg"
   import { t, locale, locales } from '../lang/i18n'
let cot 
$ : cot =$locale
</script>




    <!-- Services Start -->
    <div class="container-fluid py-6 px-5">
        <div class="text-center mx-auto mb-5" style="max-width: 600px;">
            <h1 class="display-5 mb-0">{$t("WhatWeOffer")} </h1>
            <hr class="w-25 mx-auto bg-primary">
        </div>
        <div class="row g-5">
            <div class="col-lg-4 col-md-6">
                <div class="service-item bg-secondary text-center px-5">
                    <div class="d-flex align-items-center justify-content-center bg-primary text-white rounded-circle mx-auto mb-4" style="width: 90px; height: 90px;">
                        <i class="fa fa-user-tie fa-2x"></i>
                    </div>
                    <h3 class="mb-3">{$t("SecurityCheck")}</h3>
                    <p class="mb-0">{$t("SecurityCheckDes")}</p>
                </div>
            </div>
     
            <div class="col-lg-4 col-md-6">
                <div class="service-item bg-secondary text-center px-5">
                    <div class="d-flex align-items-center justify-content-center bg-primary text-white rounded-circle mx-auto mb-4" style="width: 90px; height: 90px;">
                        <i class="fa fa-chart-area fa-2x"></i>
                    </div>
                    <h3 class="mb-3">{$t("ProductsEvaluation")} </h3>
                    <p class="mb-0">{$t("ProductsEvaluationDes")}</p>
                </div>
            </div>
    
            <div class="col-lg-4 col-md-6">
                <div class="service-item bg-secondary text-center px-5">
                    <div class="d-flex align-items-center justify-content-center bg-primary text-white rounded-circle mx-auto mb-4" style="width: 90px; height: 90px;">
                        <i class="fa fa-house-damage fa-2x"></i>
                    </div>
                    <h3 class="mb-3">{$t("TechConsultation")}</h3>
                    <p class="mb-0">{$t("TechConsultationDes")}</p>
                </div>
            </div>
        </div>
    </div>
    <!-- Services End -->


    


    <!-- Back to Top -->
    <a href="" class="btn btn-lg btn-primary btn-lg-square rounded-circle back-to-top"><i class="bi bi-arrow-up"></i></a>
