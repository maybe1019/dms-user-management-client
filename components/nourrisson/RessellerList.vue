<template>
       <div class=" py-5 space-y-[45px] flex flex-col">
              <!-- header -->
              <div class="w-full flex flex-row justify-between   font-roboto">
                     <div class=" font-roboto  leading-[28.13px] font-[400] text-[24px]">Reseller List </div>

                     <div class="flex  items-center space-x-[9px]">
                            <div class="font-roboto  leading-[25.78px] font-[400] text-[22px] text-black-dark w-[205px] ">
                                   <span>Total Erned: </span>  <span class="text-green-dark">$6800</span>
                            </div>

                            <div class="flex space-x-[18.5px]">

                                   <div class="flex items-center space-x-[8.5px] ">
                                          <div
                                                 class="font-roboto text-[14px] leading-[16.41px] font-[400] text-[#757575]">
                                                 Filter</div>

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



              </div>
              <!-- link to all projects -->


              <!-- list -->
              <div>

                     <table class="border-collapse w-full text-left ">
                            <thead>
                                   <tr class="text-[12px] text-[#212121] font-medium font-roboto  border-b">
                                          <th scope="col" class="pb-[18.75px] pt-[40px] bg-white !pl-[28px]  w-[89px]">#</th>
                                          <th scope="col" class="pb-[18.75px] pt-[40px] bg-white  w-[265px]">Executor</th>
                                          <th scope="col" class="pb-[18.75px] pt-[40px] bg-white  w-[300px]">Projects</th>
                                          <th scope="col" class="pb-[18.75px] pt-[40px] bg-white  w-[187px]">Earned</th>
                                          <th scope="col" class="pb-[18.75px] pt-[40px] bg-white  w-[227px]">Start Date/Due
                                                 Date</th>
                                          <th scope="col" class="pb-[18.75px] pt-[40px] bg-white w-[132px]">Order Status</th>
                                   </tr>
                            </thead>
                            <tbody class="font-[400] text-[14px] leading-[16.41px] text-[#212121] font-roboto">
                                   <tr class="bg-white h-[91.5px] " v-for="(item, index) in items" :key="index">
                                          <td scope="row"
                                                 class="py-0 !pl-[28px]  w-[89px] font-[400] text-[14px] leading-[16.41px] font-roboto text-gray-900 whitespace-nowrap ">
                                                 1
                                          </td>
                                          <td class="py-0 w-[265px] ">
                                                 <div class="flex items-center">
                                                        <div class="flex-none">
                                                               <img type="button"
                                                                      class="w-[40px] h-[40px] rounded-full cursor-pointer"
                                                                      src="profil.jpeg" alt="User Name" />
                                                        </div>

                                                        <div class="pl-[11px]">
                                                               <span class="text-[#212121] ">Serhii
                                                                      Movchan</span><br />
                                                               <span class="text-gray-dark leading-[20px] ">Konami</span>
                                                        </div>
                                                 </div>
                                          </td>
                                          <td class="py-0  w-[300px]">
                                                 New Projects 1
                                          </td>
                                          <td class="py-0 w-[187px]">
                                                 $200
                                          </td>
                                          <td class="py-0 w-[227px]">
                                                 <div class="flex flex-col  text-[#757575] space-y-[5px] items-start">
                                                        <div>
                                                               08/24/2019 </div>

                                                        <div>
                                                               Due 3 days ago
                                                        </div>
                                                 </div>
                                          </td>
                                          <td class="py-0 w-[132px]">
                                                 <div class="flex items-center text-blue-dark ">
                                                        <div class="h-[8px] w-[8px]  rounded-full bg-blue-dark mr-2">
                                                        </div>
                                                        in Progress
                                                 </div>
                                          </td>





                                   </tr>





                            </tbody>
                     </table>
                     <TableStepper :dataLength="70" />


              </div>
       </div>
</template>

<script>
import TableStepper from '../embrillons/TableStepper.vue';
export default {
       name: "RessellerList",
       components: { TableStepper },
       data() {
              return ({
                     name: "Serhii Movchan",

                     items: [1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 1]
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
