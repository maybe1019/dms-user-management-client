<template>
   
            <div class=" flex  justify-center mt-[3.75rem] w-full  max-w-[1250px] mx-auto sm:flex-auto">
                <div class=" w-full">
                    <Header/>
                    <div class="flex flex-row w-full  space-x-[40px] mt-[58px]">
                        <div>
                            <search/>
                        </div>
                        <div class="w-full">
                            <permission/>
                        </div>
                    </div>
                </div>
    
            </div>
       
</template>

<script>

import Header from "../../components/foeutus/designation-perm/header.vue";
import permission from "../../components/foeutus/designation-perm/permission.vue";
import search from "../../components/foeutus/designation-perm/search.vue";
export default {
    name: "DesignationPermission",
    components: {
       
        Header,
        permission,
        search


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
