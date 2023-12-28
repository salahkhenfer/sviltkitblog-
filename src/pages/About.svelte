<script>
    import { t, locale, locales } from '../lang/i18n'
let cot 
$ : cot =$locale
</script>
    <div class={`container-fluid bg-secondary p-0  ${cot == "ar" ? "durationRtl" :"durationLtr"} `} >
        <div class="row g-0 ">
            <div class="col-lg-6 py-6 px-5 durationRtl">
                <h1 class="display-5 mb-4 text-center ">{$t("WelcomeTo")} <span class="text-primary">{$t("Shawerr")}</span></h1>
                <h4 class="text-primary text-center mb-4">{$t("afterWelcome")}</h4>
                <p class="mb-4  text-center ">{$t("afterAfterWelcome")}</p>
                <a href="../contact" class="btn btn-primary d-flex  justify-content-center align-items-start  py-md-3 px-md-5 rounded-pill"> {$t("GetQuote")}</a>
            </div>
            <div class="col-lg-6">
                <div class="h-100 d-flex flex-column justify-content-center align-items-start bg-primary p-5">
                    <div class="d-flex  text-white mb-5  ">
                        <div class="d-flex  flex-shrink-0 align-items-center justify-content-center bg-white text-primary rounded-circle  mb-4" style="width: 60px; height: 60px;">
                            <i class="fa fa-user-tie fs-4  "></i>
                        </div>
                        <div class="ps-4 mx-3 ">
                            <h3  class="d-flex align-items-justify">{$t("SecurityCheck")}</h3>
                            <p class="mb-0 d-flex align-items-justify">{$t("SecurityCheckDes")}</p>
                        </div>
                    </div>
                    <div class="d-flex text-white mb-5">
                        <div class="d-flex flex-shrink-0 align-items-center justify-content-center bg-white text-primary rounded-circle mx-auto mb-4" style="width: 60px; height: 60px;">
                            <i class="fa fa-chart-line fs-4"></i>
                        </div>
                        <div class="ps-4  mx-3">
                            <h3 >{$t("ProductsEvaluation")}</h3>
                            <p class="mb-0 d-flex align-items-justify ">{$t("ProductsEvaluationDes")}</p>
                        </div>
                    </div>
                    <div class="d-flex text-white">
                        <div class="d-flex flex-shrink-0 align-items-center justify-content-center bg-white text-primary rounded-circle mx-auto mb-4" style="width: 60px; height: 60px;">
                            <i class="fa fa-balance-scale fs-4"></i>
                        </div>
                        <div class="ps-4  mx-3">
                                <h3>{$t("TechConsultation")}</h3>
                            <p  class="mb-0 d-flex align-items-justify">
                            {$t("TechConsultationDes")}
                             
                                </p>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </div>