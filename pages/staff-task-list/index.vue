<template>
    

            <div class="  flex flex-col space-y-[89px]  mt-[3.75rem] items-center w-full max-w-[1200px] mx-auto">
                <div class="w-full">
                    <StafStackBrick />
                </div>
                
                <div class="w-full">
                    <StaffAllTaskList />
                </div>


            </div>
      
</template>

<script>

import StafStackBrick from "../../components/foeutus/StafStackBrick.vue";
import StaffAllTaskList from './../../components/nourrisson/StaffAllTaskList.vue'
export default {
    name: "IndexPage",
    components: {
        
        StafStackBrick,
        StaffAllTaskList
    },
    layout:'tailwind'
};
</script>

<style scoped>

</style>
