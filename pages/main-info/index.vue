<template>
   

            <div
                class=" flex flex-col justify-between  mt-[3.75rem]  items-center w-full max-w-[1200px] mx-auto">
                <div >
                    <UserProfiler  />

                </div>
                <div class="w-full">
                <ProfilerTabs :user="'admin'" />

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
@media screen and (max-width: 900px) {
    .mycontainer {
        margin-left: 1rem;
        margin-right: 1rem;
    }
}
 
@media screen and (max-width: 900px) {
    .project-follow {
        flex-wrap: wrap;
        align-items: center;
        aspect-ratio: 50;
    }

    .project-follow div {
        width: 100%;
    }
}
</style>
