<template>
       <div class=" relative mt-[45px] ">


              <table class="w-full border-collapse   text-left  ">
                     <thead class="leading-[14.46px] text-[#212121] text-[12px] font-roboto font-medium  ">
                            <tr class="border-b">
                                   <th scope="col" class="!pl-[21.38px] w-[68px] pb-[18.75px] pt-[40px] bg-white">
                                          <div class="flex items-center">
                                                 
                                                 <CheckBox :checkType="'indeterminate'" :checked="true"
                                                        @selectAll="setSelectAll" />


            
                                          </div>
                                   </th>

                                   <th scope="col" class=" w-[46px] pb-[18.75px] pt-[40px]   bg-white">
                                          #
                                   </th>
                                   <th scope="col" class="  w-[158px] pb-[18.75px] pt-[40px] bg-white">
                                          Order Tracker ID
                                   </th>
                                   <th scope="col" class=" w-[252px] pb-[18.75px] pt-[40px] bg-white">
                                          Project
                                   </th>
                                   <th scope="col" class=" w-[231px] pb-[18.75px] pt-[40px] bg-white">
                                          Service
                                   </th>
                                   <th scope="col" class="w-[214px] pb-[18.75px] pt-[40px] bg-white">
                                          Order Date / Due Date
                                   </th>
                                   <th scope="col" class=" w-[166px] pb-[18.75px] pt-[40px] bg-white">
                                          Status
                                   </th>
                                   <th scope="col" class="  w-[65px] pb-[18.75px] pt-[40px]   bg-white">
                                          Actions
                                   </th>
                            </tr>
                     </thead>

                     <tbody class="text-[#212121] font-roboto font-[400] leading-[16.41px] text-[14px]">
                            <tr v-for="(item, index) in items" class=" hover:bg-gray-50  h-[91.5px]" :key="index">
                                   <td class="py-0 !pl-[22px]  w-[68px]">
                                          <div class="flex items-center">
                                                
                                                 <CheckBox :checkType="'determinate'" :checked="itemSelect" :key="checkKey" />
                                          </div>
                                   </td>
                                   <td class="py-0  w-[46px]">
                                          1
                                   </td>
                                   <td class="py-0  w-[158px]">
                                          234453
                                   </td>
                                   <td class="py-0 w-[252px]">
                                          English Project Edition
                                   </td>

                                   <td class=" py-0 w-[231px]">
                                          Transcription
                                   </td>
                                   <td
                                          class="py-0  w-[214px] leading-[16.41px] text-[#212121] text-[14px] font-roboto font-[400]">

                                          <div class="flex flex-col  text-[#757575] items-start">
                                                 <div>
                                                        08/24/2019 </div>

                                                 <div>
                                                        Due 3 days ago
                                                 </div>
                                          </div>

                                   </td>

                                   <td class="py-0 w-[166px]">
                                          <div
                                                 class="flex items-center  leading-[16.41px] text-[#FF8477] text-[14px] font-roboto font-[400]">
                                                 <div class="h-2.5 w-2.5  rounded-full bg-[#FF8477] mr-2">
                                                 </div>
                                                 Cancelled
                                          </div>
                                   </td>
                                   <td class="py-0  w-[65px] ">

                                          <div class="flex items-center  justify-end w-[42px] ">
                                                 <svg xmlns="http://www.w3.org/2000/svg" width="24" height="24"
                                                        fill="#757575" class="cursor-pointer" viewBox="0 0 16 16"
                                                        id="IconChangeColor">
                                                        <path d="M3 9.5a1.5 1.5 0 1 1 0-3 1.5 1.5 0 0 1 0 3zm5 0a1.5 1.5 0 1 1 0-3 1.5 1.5 0 0 1 0 3zm5 0a1.5 1.5 0 1 1 0-3 1.5 1.5 0 0 1 0 3z"
                                                               id="mainIconPathAttribute" fill="#757575"></path>
                                                 </svg>
                                          </div>


                                   </td>
                            </tr>







                     </tbody>
              </table>


              <!-- Table  stepper -->
              <TableStepper :dataLength="70" />
              <!-- end stepeper -->
       </div>
</template>

<script>
       import CheckBox from '../../components/embrillons/CheckBox.vue';
import TableStepper from '../../components/embrillons/TableStepper.vue';
export default {
       name: "OrderList",
       components: {
              TableStepper,
              CheckBox
              
       },

       data() {
              return ({
                     name: "Serhii Movchan",
                     itemSelect: false,
                     checkKey:0,
                     items: [1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 1]

              })
       },
        
       methods: { 
              setSelectAll(val) {
                     console.log("select all state", val)
                     if (val) {
                            this.itemSelect = true
                                  this.checkKey += 1;



                     } else {
                            this.itemSelect = false
                                  this.checkKey += 1;

                     }

              }
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
