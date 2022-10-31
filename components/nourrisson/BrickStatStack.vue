<template>
 
  <div class="grid gap-[10px]   grid-cols-4 grid-rows-2">
    <DashStatBrick />
    <DashStatBrick />
    <DashStatBrick />
    <DashStatBrick />
   
  
    <DashStatBrick />
    <DashStatBrick />
    <DashStatBrick />
    <DashStatBrick />
  
 </div>

</template>
<script>
import DashStatBrick from "../embrillons/DashStatBrick.vue";
export default {
  name: "BrickStatStack",
  components: {
    DashStatBrick,
  },
};
</script>
<style scoped>


@media screen and (max-width:752px ) {
  
 
}

</style>
