<script setup>
import SectionBase from './SectionBase.vue'
import Article from './Article.vue'

import ImageConfetti from '@/assets/images/image-confetti.jpg'
import ImageCurrency from '@/assets/images/image-currency.jpg'
import ImagePlane from '@/assets/images/image-plane.jpg'
import ImageRestaurant from '@/assets/images/image-restaurant.jpg'

</script>
<template>
    <SectionBase>
        <h2>Latest Articles</h2>
        <Article author="Claire Robinson" title="Receive money in any currency with no fees" :img="ImageConfetti">
            The world is getting smaller and we’re becoming more mobile. So why should you be 
            forced to only receive money in a single …
        </Article>
        <Article author="Wilson Hutton" title="Treat yourself without worrying about money" :img="ImageCurrency">
            Our simple budgeting feature allows you to separate out your spending and set 
            realistic limits each month. That means you …
        </Article>
        <Article author="Wilson Hutton" title="Take your Easybank card wherever you go" :img="ImagePlane">
            We want you to enjoy your travels. This is why we don’t charge any fees on purchases 
            while you’re abroad. We’ll even show you …
        </Article>
        <Article author="Claire Robinson" title="Our invite-only Beta accounts are now live!" :img="ImageRestaurant">
            After a lot of hard work by the whole team, we’re excited to launch our closed beta. 
            It’s easy to request an invite through the site …
        </Article>
    </SectionBase>
</template>