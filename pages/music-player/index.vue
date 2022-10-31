<template>
    
    
            <div class=" flex flex-col justify-between  mt-[3.75rem]  items-center w-full  max-w-[1200px] mx-auto">
                
              <div class="w-full">
                     <MusicTabs/>
              </div>
            </div>
    
    
    
      
</template>

<script>

import MusicTabs from '../../components/foeutus/music-player/MusicTabs.vue';
export default {
    name: "MuzicPlayer",
    components: {
        MusicTabs
       
    },
    layout:'tailwind'
};
</script>

<style scoped>

</style>
