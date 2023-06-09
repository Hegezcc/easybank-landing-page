<script setup>
import SectionBase from './SectionBase.vue';
import Point from './Point.vue';

import IconOnline from '@/assets/images/icon-online.svg';
import IconBudgeting from '@/assets/images/icon-budgeting.svg';
import IconOnboarding from '@/assets/images/icon-onboarding.svg';
import IconApi from '@/assets/images/icon-api.svg';

</script>
<template>
    <SectionBase>
        <h2>Why choose Easybank?</h2>
        <p>
            We leverage Open Banking to turn your bank account into your financial hub. Control 
            your finances like never before.
        </p>
        <div class="items">
            <Point title="Online Banking" :img="IconOnline">
                Our modern web and mobile applications allow you to keep track of your finances 
                wherever you are in the world.
            </Point>
            <Point title="Simple Budgeting" :img="IconBudgeting">
                See exactly where your money goes each month. Receive notifications when you’re 
                close to hitting your limits.
            </Point>
            <Point title="Fast Onboarding" :img="IconOnboarding">
                We don’t do branches. Open your account in minutes online and start taking control 
                of your finances right away.
            </Point>
            <Point title="Open API" :img="IconApi">
                Manage your savings, investments, pension, and much more from one account. Tracking 
                your money has never been easier.
            </Point>
        </div>
    </SectionBase>
</template>