<template>
    <div class="flex flex-col space-y-[5px]">

<div class="w-full">
<TaskInformation/>
    
</div>


       <div class=" flex justify-between flex-row space-x-[8px] w-full sm:space-x-0 sm:flex-wrap">
              <WorkFile/>
        <PreviewSetting/>
       </div> 
        
    </div>
</template>

<script>
import TaskInformation from '../foeutus/music-player/TaskInformation.vue';
import WorkFile from '../foeutus/music-player/WorkFile.vue';
import PreviewSetting from '../foeutus/music-player/PreviewSetting.vue';
export default {
    name: "WorkSpace",
    components: {
        WorkFile,
        PreviewSetting,
        TaskInformation
        
    }
};
</script>

<style scoped>

</style>
 