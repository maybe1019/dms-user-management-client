<template>
    <!-- body containner -->

    <div class="flex flex-col mt-[3.75rem] justify-between items-center w-full space-y-[98px] max-w-[1200px] mx-auto">
        <div class="w-full">
            <BrickStatStack />
        </div>
        <div class="w-full myStat">
            <ActivitiesTask />
        </div>
        <div class="w-full ">
            <otherTaskActivity />
        </div>
        <div class="w-full ">
            <LastActivity />
        </div>
        <!-- project and task llist -->

    </div>
</template>

<script>
import LastActivity from '../../components/foeutus/second-staff-dash/LastActivity.vue'
import ActivitiesTask from '../../components/foeutus/second-staff-dash/ActivitiesTask.vue'
import otherTaskActivity from '../../components/foeutus/second-staff-dash/otherTaskActivity.vue'
import BrickStatStack from '../../components/nourrisson/BrickStatStack.vue'

export default {
    name: 'IndexPage',
    components: {
        BrickStatStack,

        ActivitiesTask,
        otherTaskActivity,
        LastActivity
    },
    layout: 'tailwind',
}
</script>

<style scoped>
</style>
