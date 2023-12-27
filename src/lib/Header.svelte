
<script>
import { t, locale, locales  } from '../lang/i18n'

let cot 
$ : cot =$locale

</script>

<header class={`px1 py2 md:p2 ${cot == "ar" ? "durationRtl" :""} `}>
  <h1 class="h1 lh1 lsh"><slot /></h1>
</header>
