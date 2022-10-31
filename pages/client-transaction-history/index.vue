<template>
    

            <div class="  flex flex-col mt-[3.75rem] space-y-[89px]   items-center w-full max-w-[1200px] mx-auto">
                <div class="w-full">
                    <StafStackBrick />
                </div>
                
                <div class="w-full">
                    <ClientTransactionHistory />
                </div>


            </div>
      
</template>

<script>

import StafStackBrick from "../../components/foeutus/StafStackBrick.vue";
import ClientTransactionHistory from './../../components/nourrisson/ClientTransactionHistory.vue'
export default {
    name: "IndexPage",
    components: {
        
        StafStackBrick,
        ClientTransactionHistory
    },
    layout:'tailwind'
};
</script>

<style scoped>

</style>
