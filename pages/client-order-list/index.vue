<template>


    <div class="  flex flex-col justify-between  mt-[3.75rem] items-center w-full max-w-[1200px] mx-auto">
        <div class="w-full">
            <StafStackBrick />
        </div>
        <div class="w-full">
            <HeaderFilter />
        </div>
        <div class="w-full">
            <OrderList />
        </div>


    </div>

</template>

<script>

import HeaderFilter from "../../components/foeutus/client-order/HeaderFilter.vue";
import StafStackBrick from "../../components/foeutus/StafStackBrick.vue";
import OrderList from './OrderList.vue'
export default {
    name: "IndexPage",
    components: {
        HeaderFilter,
        StafStackBrick,
        OrderList
    },
    layout: 'tailwind'
};
</script>

<style scoped>
</style>
