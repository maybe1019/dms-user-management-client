<template>
    

            <div class="  flex flex-col justify-between mt-[3.75rem]  items-center w-full mx-auto  max-w-[1200px] sm:max-w-[1200px]">
                <div class="w-full">
                    <StafStackBrick />
                </div>
                <div class="w-full">
                    <StafFilter />
                </div>
                <div class="w-full">
                    <AllStaff />
                </div>


            </div>
      
</template>

<script>
import StafStackBrick from "../../components/foeutus/StafStackBrick.vue";
import StafFilter from "./../../components/foeutus/StafFilter.vue";
import AllStaff from './../../components/nourrisson/AllStaf.vue'
export default {
    name: "IndexPage",
    components: {

        StafStackBrick,
        StafFilter,
        AllStaff
    },
    layout:'tailwind'
};
</script>

<style scoped>

</style>
