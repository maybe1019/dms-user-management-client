
<template>
       <div class="mt-[45px]">
              <table class="w-full  border-collapse  text-left  ">
                     <thead class=" ">
                            <tr
                                   class="border-none   leading-[14.46px] text-[#212121] text-[12px] font-roboto font-medium">


                                   <th scope="col" class="pt-[40px]  pb-[20px]  !pl-[20px] w-[134px] bg-white">
                                          Job ID
                                   </th>
                                   <th scope="col" class="pt-[40px]  pb-[20px] w-[236px] bg-white">
                                          Task Name
                                   </th>
                                   <th scope="col" class="pt-[40px]  pb-[20px] w-[152px] bg-white">
                                          Staff Assigned
                                   </th>

                                   <th scope="col" class="pt-[40px]  pb-[20px] w-[196px] bg-white">
                                          Create/Due Date
                                   </th>
                                   <th scope="col" class="pt-[40px]  pb-[20px] w-[109px] bg-white">
                                          Order Status
                                   </th>


                            </tr>


                     </thead>

                     <tbody class="leading-[16.41px] text-[#212121] text-[14px] font-roboto font-[400]">
                            <tr v-for="(item, index) in items" :key="item" class=" h-[91.5px] hover:bg-gray-50 ">

                                   <td class="py-0  !pl-[20px] w-[134px]  ">
                                          
                                                 #42343
                                          

                                   </td>

                                   <td class="py-0  w-[236px] ">
                                          
                                                 Task Name Number 1
                                          

                                   </td>
                                   <td class="py-0 w-[152px]">
                                          
                                                 <a href="" class="text-blue-dark underline">5</a>
                                          

                                   </td>
                                   <td class="py-0  w-[196px]">
                                          <div class=" text-[#757575] flex items-center   border-b-[#C4C4C4] ">
                                                
                                                <div class=" space-y-[3px] flex flex-col">
                                                 <span>08/24/2019</span>
                                                 <span> 02:30 PM</span>
                                                </div> 
                                          </div>
                                   </td>




                                   <td class="py-0 w-[109px] ">
                                          <div class="flex items-center text-blue-dark ">
                                                 <div class="h-[8px] w-[8px]  rounded-full bg-blue-dark mr-[10px]">
                                                 </div>
                                                 <span class="w-[85px]">in Progress</span>
                                                 
                                          </div>
                                   </td>

                            </tr>






                     </tbody>
              </table>


              <TableStepper :dataLength="70" />




       </div>
</template>
<script>
import TableStepper from '../../embrillons/TableStepper.vue';
export default {
       name: "TaskTable",
       components: {
              TableStepper
       },
       data() {
              return ({

                     items: [1, 1, 1, 1, 1, 1, 1, 1, 1]
              })
       }
};
</script>
<style scoped>
tr th,
tr td {
       border-top: none;
       border-left: none;
       border-right: none;
       padding-right: 0px;
       padding-left: 0px;
}

table th {

       position: sticky;
       top: 0 !important;
       margin-top: 0px !important;
       z-index: 0;
}
</style>
