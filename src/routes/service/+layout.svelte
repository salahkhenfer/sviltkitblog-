<script>
    /** @type {import('./$types').LayoutData} */
    export let data;
    import { t  } from "../../lang/i18n"

</script>

    <!-- Page Header Start -->
    <div class="container-fluid bg-dark p-5">
        <div class="row">
            <div class="col-12 text-center">
                <h1 class="display-4 text-white">{$t("SERVICE")}</h1>
           
            </div>
        </div>
    </div>
    <slot/>
    <!-- Page Header End -->
    