<template>
   
    
                <div class="  mt-[3.75rem] w-full max-w-[1200px] mx-auto">
                    <FilterHeader/>
    
                </div>
                
            
        
   
</template>

<script>

import FilterHeader from "../../components/nourrisson/designation/FilterHeader.vue";
export default {
    name: "MainInfo",
    components: {
        
        FilterHeader


    },
    layout:'tailwind'
};
</script>

<style scoped>
@media screen and (max-width: 900px) {
    .mycontainer {
        margin-left: 1rem;
        margin-right: 1rem;
    }
}

@media screen and (max-width: 900px) {
    .project-follow {
        flex-wrap: wrap;
        align-items: center;
        aspect-ratio: 50;
    }
    .project-follow div {
        width: 100%;
    }
}
</style>
