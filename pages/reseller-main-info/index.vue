<template>
   

            <div
                class=" flex flex-col justify-between  mt-[3.75rem]  items-center w-full max-w-[1200px] mx-auto">
                <div >
                    <UserProfiler  />

                </div>
                <div class="w-full">
                <ProfilerTabs :user="'reseller'" />

                </div>

            </div>
        
</template>

<script>

import UserProfiler from "./../../components/foeutus/UserProfiler.vue"
import ProfilerTabs from "./../../components/foeutus/ProfilerTabs.vue"
export default {
    name: "MainInfo",
    components: {
      
        UserProfiler,
        ProfilerTabs

    },
    layout:'tailwind'
};
</script>

<style scoped>

</style>
