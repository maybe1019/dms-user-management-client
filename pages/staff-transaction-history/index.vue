<template>
    

            <div class="  flex flex-col space-y-[89px] mt-[3.75rem]  items-center w-full max-w-[1200px] mx-auto">
                <div class="w-full">
                    <StafStackBrick />
                </div>
                
                <div class="w-full">
                    <StaffTransaction />
                </div>


            </div>
      
</template>

<script>

import StafStackBrick from "../../components/foeutus/StafStackBrick.vue";
import StaffTransaction from './../../components/nourrisson/StaffTransaction.vue'
export default {
    name: "IndexPage",
    components: {
        
        StafStackBrick,
        StaffTransaction
    },
    layout:'tailwind'
};
</script>

<style scoped>

</style>
