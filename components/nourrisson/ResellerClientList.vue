<template>
       <div class=" relative space-y-[48px]  ">
              <div class="flex flex-row justify-between items-center project-header font-roboto">
                     <div class=" font-roboto  leading-[28.13px] font-[400] text-[24px]">Client List </div>


                     <div class="flex space-x-[18.5px]">

                            <div class="flex items-center space-x-[8.5px]">
                                   <div class="font-roboto text-[14px] leading-[16.41px] font-[400] text-[#757575]">
                                          Filter
                                   </div>

                                   <div class="cursor-pointer w-[20px] h-[20px]">
                                          <svg viewBox="0 0 48 48" xmlns="http://www.w3.org/2000/svg">
                                                 <path d="M6 36h12v-4h-12v4zm0-24v4h36v-4h-36zm0 14h24v-4h-24v4z"
                                                        fill="#757575" />
                                                 <path d="M0 0h48v48h-48z" fill="none" />
                                          </svg>
                                   </div>
                            </div>
                            <div class="flex items-center space-x-[8.5px]">
                                   <span
                                          class="font-roboto text-[14px] leading-[16.41px] font-[400] text-[#757575]">Sort</span>

                                   <div class="cursor-pointer w-[20px] h-[20px] ">
                                          <svg viewBox="0 0 48 48" xmlns="http://www.w3.org/2000/svg">
                                                 <path d="M6 36h12v-4h-12v4zm0-24v4h36v-4h-36zm0 14h24v-4h-24v4z"
                                                        fill="#757575" />
                                                 <path d="M0 0h48v48h-48z" fill="none" />
                                          </svg>
                                   </div>
                            </div>
                     </div>



              </div>

              <table class="table  w-full border-collapse   text-left  ">
                     <thead class="  ">
                            <tr
                                   class="border-none leading-[14.46px] text-[#212121] text-[12px] font-roboto font-medium">


                                   <th scope="col" class=" pb-[18.75px] pt-[40px] bg-white !pl-[28px] w-[91px]  ">
                                          #
                                   </th>
                                   <th scope="col" class=" pb-[18.75px] pt-[40px] bg-white w-[89px]">
                                          ID
                                   </th>
                                   <th scope="col" class=" pb-[18.75px] pt-[40px] bg-white w-[268px]">
                                          Staff
                                   </th>
                                   <th scope="col" class=" pb-[18.75px] pt-[40px] bg-white w-[267px]">
                                          Projects
                                   </th>
                                   <th scope="col" class=" pb-[18.75px] pt-[40px] bg-white w-[250px]">
                                          Email
                                   </th>
                                   <th scope="col" class=" pb-[18.75px] pt-[40px] bg-white  w-[164px]">
                                          Last Activity
                                   </th>
                                   <th scope="col" class="  pb-[18.75px] pt-[40px]  w-[71px]   bg-white">
                                          Actions
                                   </th>

                            </tr>
                     </thead>

                     <tbody class="leading-[16.41px] text-[#212121] text-[14px] font-roboto font-[400]">
                            <tr class=" h-[91.5px] hover:bg-gray-50 " v-for="(item, index) in items" :key="index">

                                   <td class="py-0 !pl-[28px] w-[91px] ">
                                          1
                                   </td>
                                   <td class="py-0 w-[89px]">
                                          23245
                                   </td>


                                   <td class="py-0 w-[268px]">

                                          <div class="flex items-center">
                                                 <div class="flex-none">
                                                        <img type="button" class="w-[40px] h-[40px] rounded-full cursor-pointer"
                                                               src="profil.jpeg" alt="User Name" />
                                                 </div>

                                                 <div class="pl-[11px]">
                                                        <span class="text-[#212121] leading-[24px] ">Serhii
                                                               Movchan</span><br />
                                                        <span class="text-[#BDBDBD] leading-[20px] w-[147px] ">Limited Techologies</span>
                                                 </div>
                                          </div>
                                   </td>
                                   <td class="py-0  w-[267px]">
                                          2 Projects  <a href="" class="underline text-blue-dark">View Details</a>
                                   </td>
                                   <td class="py-0  w-[250px]">
                                          <a href="" class="underline text-blue-dark">example@gmail.com</a>
                                   </td>
                                   <td class="py-0  w-[164px] text-gray-dark">
                                          Due 2 days ago
                                   </td>
                                   <td class="py-0  w-[71px]  ">
                                          <div class="flex justify-end w-[41px]">
                                                 <svg xmlns="http://www.w3.org/2000/svg" class="h-6 w-6 cursor-pointer"
                                                        fill="none" viewBox="0 0 24 24" stroke="#757575"
                                                        stroke-width="2">
                                                        <path stroke-linecap="round" stroke-linejoin="round"
                                                               d="M5 12h.01M12 12h.01M19 12h.01M6 12a1 1 0 11-2 0 1 1 0 012 0zm7 0a1 1 0 11-2 0 1 1 0 012 0zm7 0a1 1 0 11-2 0 1 1 0 012 0z" />
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
import TableStepper from '../embrillons/TableStepper.vue';
export default {
       name: "RessellerClientList",
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
