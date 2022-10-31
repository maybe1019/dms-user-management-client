<template>
    <!-- body containner -->





    <div class=" flex flex-col justify-between mt-[3.75rem]  items-center w-full max-w-[1200px]  mx-auto ">
        <div class="w-full">
            <BrickStatStack />
        </div>

        
            <div class=" w-full min-w-[800px] graph">

                <LineGraph />


            </div>
        


        <!-- project and task llist -->
        <div class="w-full flex flex-row space-x-[153px] mt-[90px] flex-wrap sm:space-x-0 ">
            <div>
                <StaffTaskListSide />
            </div>
            <div>
                <StaffActivesOrders />
            </div>
        </div>

    </div>
</template>

<script>
import LineGraph from './../../components/foeutus/LineGraph.vue'

import BrickStatStack from "../../components/nourrisson/BrickStatStack.vue";
import StaffActivesOrders from "../../components/nourrisson/StaffActivesOrders.vue";
import StaffTaskListSide from "../../components/nourrisson/StaffTaskListSide.vue";
export default {
    name: "IndexPage",
    components: {
        BrickStatStack,
        StaffActivesOrders,
        StaffTaskListSide,
        LineGraph
    },
    layout: 'tailwind',

};
</script>

<style scoped>
     .graph{
        
        width:100% ;
            }
</style>
