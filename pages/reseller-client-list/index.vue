<template>
    

            <div class="  flex flex-col space-y-[89px]  mt-[3.75rem] items-center w-full max-w-[1200px] mx-auto">
                <div class="w-full">
                    <StafStackBrick />
                </div>
                
                <div class="w-full">
                    <ResellerClientList />
                </div>


            </div>
      
</template>

<script>
import ResellerClientList from "../../components/nourrisson/ResellerClientList.vue";
import StafStackBrick from "../../components/foeutus/StafStackBrick.vue";
export default {
    name: "IndexPage",
    components: {
        
        StafStackBrick,
        ResellerClientList
    },
    layout:'tailwind'
};
</script>

<style scoped>

</style>
