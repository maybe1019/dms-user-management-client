<template>



    <!-- body containner -->





    <div class=" flex flex-col justify-between  mt-[3.75rem] items-center w-full   max-w-[1200px] mx-auto ">
        <div class="w-full">
            <BrickStatStack />
        </div>
        <div class="graph">
            <div class="w-full min-w-[800px]">

                <Stat />


            </div>
        </div>

        <!-- project and task llist -->
        <div class="w-full flex flex-row justify-between  mt-[90px] flex-wrap ">
            <div>
                <ProjectListSide />
            </div>
            <div>
                <TaskListSide />
            </div>
        </div>

    </div>









</template>

<script>
import BrickStatStack from "../components/nourrisson/BrickStatStack.vue";
import Stat from "../components/foeutus/StatGraph.vue";
import ProjectListSide from "../components/nourrisson/ProjectListSIde.vue";
import TaskListSide from "../components/nourrisson/TaskListSide.vue";
export default {
    name: "IndexPage",
    components: {
       
        BrickStatStack,
        Stat,
        ProjectListSide,
        TaskListSide,
    },
    layout: 'tailwind',

};
</script>

<style scoped>
.mycontainer {
    /* max-width: 90rem; */
    overflow: auto !important;
}

/* .myStat {
    height: 40%;
} */

.project-info {
    /* transform: translateY(-30px); */
}

@media screen and (min-width : 1000px) {
    .graph{
        
width:100% ;
max-width: 1200px;
    }
    
}
@media screen and (max-width : 1000px) {
    .graph{
width: 100%;        
    }
    
}

</style>
