<template>
    <div>
        <div class="partner-logo">
        <div class="container">
            <carousel class="logo-carousel" :autoplay="true" :items="5" :loop="true" :dots="false" :nav="false">
                <div class="logo-item">
                    <div class="tablecell-inner">
                        <img src="img/logo-carousel/logo-1.png" alt="" />
                    </div>
                </div>
                <div class="logo-item">
                    <div class="tablecell-inner">
                        <img src="img/logo-carousel/logo-2.png" alt="" />
                    </div>
                </div>
                <div class="logo-item">
                    <div class="tablecell-inner">
                        <img src="img/logo-carousel/logo-3.png" alt="" />
                    </div>
                </div>
                <div class="logo-item">
                    <div class="tablecell-inner">
                        <img src="img/logo-carousel/logo-4.png" alt="" />
                    </div>
                </div>
                <div class="logo-item">
                    <div class="tablecell-inner">
                        <img src="img/logo-carousel/logo-5.png" alt="" />
                    </div>
                </div>
            </carousel>
        </div>
    </div>
    </div>
</template>

<script>
    import carousel from 'vue-owl-carousel'
    export default{
        name : "PartnerLogo",
        components : {
            carousel
        }
    }
</script>