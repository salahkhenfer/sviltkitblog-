<script>

import App from "../lang/App.svelte"
import { t, locale, locales  } from '../lang/i18n'
let cot 
$ : cot =$locale
</script>

<style>

.navbar-br {
  
  margin-left: 50%;

}
</style>
<!-- Header Start -->
    <nav class={ ` ${cot == "ar" ? "durationRtl" :""}   navbar navbar-expand-lg bg-white navbar-light shadow-sm px-5 py-3 py-lg-0 `  }
  
  >


         <a href="/" class={`navbar-brand ${cot == "ar" ? "navbar-br" : ""}    p-0`}>
             <h1 class="m-0 text-uppercase text-primary">{$t("Shawerr")} </h1>
         </a>
    


        <div  class="collapse navbar-collapse " id="navbarCollapse">
            <div class="navbar-nav ms-auto py-0 me-n3">
                <a href="/" class="nav-item nav-link">{$t("HOME")}</a>
                <a href="/about" class="nav-item nav-link"> {$t("ABOUT")}</a>
                <a href="/service" class="nav-item nav-link">{$t("SERVICE")}</a>

                    <a href="/blogs" class="nav-link ">{$t("BLOG")}</a>
                    
                    <a href="/contact" class="nav-item nav-link">{$t("CONTACT")}</a>
                    <App/>
            </div>
        </div>
    </nav>