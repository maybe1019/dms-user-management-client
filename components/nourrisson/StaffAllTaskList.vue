<template>
       <div class=" relative space-y-[48px]   w-full">
              <div class="flex flex-row justify-between items-center project-header font-roboto">
                     <div class=" font-roboto  leading-[25.78px] font-[400] text-[22px]">Task List</div>


                     <div class="flex space-x-[18.5px]">

                            <div class="flex items-center space-x-[8.5px]">
                                   <div class="font-roboto text-[14px] leading-[16.41px] font-[400] text-[#757575]">
                                          Filter
                                   </div>

                                   <div class="cursor-pointer w-[20px] h-[20px]">
                                          <svg viewBox="0 0 48 48" xmlns="http://www.w3.org/2000/svg" class="w-full h-full">
                                                 <path d="M6 36h12v-4h-12v4zm0-24v4h36v-4h-36zm0 14h24v-4h-24v4z"
                                                        fill="#757575" />
                                                 <path d="M0 0h48v48h-48z" fill="none" />
                                          </svg>
                                   </div>
                            </div>
                            <div class="flex items-center space-x-[8.5px]">
                                   <span
                                          class="font-roboto text-[14px] leading-[16.41px] font-[400] text-[#757575]">Sort</span>

                                   <div class="cursor-pointer w-[20px] h-[20px] " >
                                          <svg viewBox="0 0 48 48" xmlns="http://www.w3.org/2000/svg" class="w-full h-full" stroke="3">
                                                 <path d="M6 36h12v-4h-12v4zm0-24v4h36v-4h-36zm0 14h24v-4h-24v4z"
                                                        fill="#757575" />
                                                 <path d="M0 0h48v48h-48z" fill="none" />
                                          </svg>
                                   </div>
                            </div>
                     </div>



              </div>

              <table class="w-full border-collapse   text-left  ">
                     <thead class="">
                            <tr
                                   class="  leading-[14.46px] text-[#212121] text-[12px] font-roboto font-medium border-b ">


                                   <th scope="col" class="pb-[20.25px] pt-[40px]  !pl-[40px] w-[178px] bg-white  ">
                                          Order ID
                                   </th>
                                   <th scope="col" class="pb-[20.25px] pt-[40px]   w-[137px] bg-white  ">
                                          Job ID
                                   </th>
                                   <th scope="col" class="pb-[20.25px] pt-[40px]   w-[253px] bg-white  ">
                                          Task Name
                                   </th>
                                   <th scope="col" class="pb-[20.25px] pt-[40px]  w-[269px] bg-white  ">
                                          Staff
                                   </th>
                                   <th scope="col" class="pb-[20.25px] pt-[40px]   w-[207px] bg-white  ">
                                          Create/Due Date
                                   </th>
                                   <th scope="col" class="pb-[20.25px] pt-[40px]   w-[156px]  bg-white  ">
                                          Order Status
                                   </th>

                            </tr>
                     </thead>

                     <tbody class="leading-[16.41px] text-[#212121] text-[14px] font-roboto font-[400] ">
                            <tr v-for="(item, index) in items" class=" hover:bg-gray-50 h-[91.5px] " :key="index">

                                   <td class="py-0 !pl-[40px]  w-[178px]">
                                          234453
                                   </td>
                                   <td class="py-0 w-[137px]">
                                          #42343
                                   </td>

                                   <td class="py-0 w-[253px]">
                                          Task Name Number 1
                                   </td>
                                   <td class="py-0 w-[269px] ">

                                          <div class="flex flex-none items-center">
                                                 <div class="flex-none">
                                                        <img type="button" class="w-[40px] h-[40px] rounded-full cursor-pointer"
                                                               src="profil.jpeg" alt="User Name" />
                                                 </div>

                                                 <div class="ml-[11px]">
                                                        <span
                                                               class="  font-roboto p-username text-[14px] text-[#212121] font-[400] ">{{
                                                                             name
                                                               }}</span><br />
                                                        <span class=" text-[#757575]">Manager</span>
                                                 </div>
                                          </div>
                                   </td>
                                   <td class="py-0  w-[207px]">
                                          <div class="flex flex-col space-y-[5px]  text-[#757575] items-start">
                                                 <div>
                                                        08/24/2019 </div>

                                                 <div>
                                                        Due 3 days ago
                                                 </div>
                                          </div>
                                   </td>
                                   <td class="py-0 w-[156px]  ">
                                          <div class="flex items-center text-blue-dark">
                                                 <div class="h-[8px] w-[8px]  rounded-full bg-blue-dark mr-[10px]">
                                                 </div>
                                                 in Production
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
import TableStepper from '../embrillons/TableStepper.vue';
export default {
       name: "StaffAllTaskList",
       components: {
              TableStepper
       },

       data() {
              return ({
                     name: "Serhii Movchan",

                     items: [1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 1]
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
