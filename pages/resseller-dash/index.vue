<template>
    <!-- body containner -->





    <div class=" flex flex-col justify-between  mt-[3.75rem]  items-center w-full max-w-[1200px] mx-auto ">
        <div class="w-full">
            <BrickStatStack />
        </div>
        <div class="w-full">
            <div class="w-full min-w-[800px] myStat">

                <RessellerLineGraph />


            </div>

        </div>

    

    <!-- project and task llist -->
    <div class=" w-full  mt-[90px] ">
        <div>
            <RessellerList />
        </div>

    </div>

    </div>
</template>

<script>
import RessellerList from './../../components/nourrisson/RessellerList.vue'
import RessellerLineGraph from "../../components/foeutus/RessellerLineGraph.vue";
import BrickStatStack from "../../components/nourrisson/BrickStatStack.vue";
import StaffActivesOrders from "../../components/nourrisson/StaffActivesOrders.vue";
import StaffTaskListSide from "../../components/nourrisson/StaffTaskListSide.vue";
export default {
    name: "IndexPage",
    components: {
        BrickStatStack,
        StaffActivesOrders,
        StaffTaskListSide,
        RessellerLineGraph,
        RessellerList
    },
    layout: 'tailwind',

};
</script>

<style scoped>
</style>
