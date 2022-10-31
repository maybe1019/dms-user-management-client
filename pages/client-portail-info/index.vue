<template>
    
    
            <div class=" flex flex-col mt-[3.75rem]   items-center w-full  max-w-[1200px] mx-auto ">
                
              <div class="w-full">
                     <PortailHeaderVue/>
              </div>
               <div class="w-full">
                     <PortailTabs/>
              </div>
               
            </div>
    
    
    
      
</template>

<script>

import PortailHeaderVue from '../../components/foeutus/client-portail/PortailHeader.vue';
import PortailTabs from '../../components/foeutus/client-portail/PortailTabs.vue';
export default {
    name: "MuzicPlayer",
    components: {
      PortailHeaderVue,
        PortailTabs
       
    },
    layout:'tailwind'
};
</script>

<style scoped>

</style>
