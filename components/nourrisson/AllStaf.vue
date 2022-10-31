<template>
       <div class="  mt-[45px] ">


              <table class=" border-collapse    text-left  ">
                     <thead class=" ">

                            <tr class=" border-b   leading-[14.46px] text-[#212121] text-[12px] font-roboto ">
                                   <th  class="  pb-[18.75px] !pl-[21.37px] w-[68px] pt-[40px]    bg-white">
                                          

                                                 <CheckBox :checkType="'indeterminate'" :checked="true"
                                                        @selectAll="setSelectAll" />


                                          
                                   </th>

                                   <th 
                                          class=" pb-[18.75px]  w-[46px]    pt-[40px] bg-white   ">
                                          #
                                   </th>
                                   <th  class="pb-[18.75px]  w-[251px]   bg-white pt-[40px] ">
                                          Name
                                   </th>
                                   <th  class="pb-[18.75px] w-[200px]    bg-white pt-[40px] ">
                                          Designation
                                   </th>
                                   <th  class="pb-[18.75px]  w-[192px]    bg-white pt-[40px] ">
                                          Phone
                                   </th>
                                   <th  class="pb-[18.75px]  w-[214px]   bg-white pt-[40px] ">
                                          Task Inprogress
                                   </th>
                                   <th  class="pb-[18.75px]  w-[166px]   bg-white pt-[40px] ">
                                          Status
                                   </th>
                                   <th 
                                          class=" pb-[18.75px]  w-[65px]    bg-white pt-[40px] ">
                                          Actions
                                   </th>
                            </tr>

                     </thead>

                     <tbody>

                            


                            <tr class=" hover:bg-gray-50 h-[92px] font-[400]" v-for="(item,index) in items" :key="index">
                                   <td class=" w-[68px]   !pl-[21.37px] py-0  ">
                                          

                                                 <CheckBox :checkType="'determinate'" :checked="itemSelect"
                                                        :key="checkKey" />
                                          
                                   </td>
                                   <td class="  w-[46px]    py-0  text-[#212121] font-roboto  leading-[16.41px] ">
                                          
                                                 1

                                          
                                   </td>
                                   <td class="w-[251px]     py-0 ">
                                          <div class="flex flex-none items-center   ">
                                                 <div class="flex-none">
                                                        <img type="button"
                                                               class="w-[40px] h-[40px] rounded-full cursor-pointer"
                                                               src="profil.jpeg" alt="User Name" />
                                                 </div>

                                                 <div class="pl-[10px] flex flex-col space-y-[0px]">
                                                        <span
                                                               class="  font-roboto text-[14px] leading-[24px] text-black-dark ">{{
                                                                             name
                                                               }}</span>
                                                        <span
                                                               class="leading-[20px] font-roboto  fomt-normal  text-[14px] text-[#BDBDBD]">example@gmail.com</span>
                                                 </div>
                                          </div>
                                   </td>

                                   <td
                                          class="  w-[200px]  py-0 leading-[16.41px] text-[#212121] text-[14px] font-roboto  ">

                                          
                                                 Proofreader
                                          

                                   </td>
                                   <td
                                          class="  w-[192px]     py-0 leading-[16.41px] text-[#212121] text-[14px] font-roboto ">
                                          <div class="w-[103px]">
                                                 +380994243223
                                          </div>
                                          
                                                

                                          

                                   </td>
                                   <td class=" w-[214px]  py-0">
                                          <div
                                                 class="flex flex-col items-start justify-center    w-[79px] flex-none space-y-[0px]">
                                                 <span href="#"
                                                        class="text-blue-dark  leading-[18px] text-[13px] font-roboto font-[400] underline">English
                                                        Task</span>
                                                 <span href="#"
                                                        class="leading-[18px] text-[13px] font-roboto  text-[#4489FE] font-[400]  underline ">Spanish
                                                        Task</span>
                                                        <span href="#"
                                                        class="leading-[18px] text-[13px] font-roboto  text-[#4489FE] font-[400] ">+5 More Task </span>

                                          </div>

                                   </td>
                                   <td class=" w-[166px]  py-0">
                                          <div
                                                 class="flex items-center     leading-[16.41px] text-green-dark text-[14px] font-roboto ">
                                                 <div class="h-[8px] w-[8px]  rounded-full bg-[#0FAA58] mr-[10px]">
                                                 </div>
                                                <span class="w-[85px]">active </span>  
                                          </div>
                                   </td>
                                   <td class=" w-[65px] py-0 ">
                                          <div class="flex    w-[42px]  items-center justify-end ">

                                                 <svg fill="none" height="16" viewBox="0 0 16 16" width="16"
                                                        xmlns="http://www.w3.org/2000/svg">
                                                        <path d="M10 8C10 9.10457 9.10457 10 8 10C6.89543 10 6 9.10457 6 8C6 6.89543 6.89543 6 8 6C9.10457 6 10 6.89543 10 8Z"
                                                               fill="#757575" />
                                                        <path d="M4 8C4 9.10457 3.10457 10 2 10C0.895431 10 0 9.10457 0 8C0 6.89543 0.895431 6 2 6C3.10457 6 4 6.89543 4 8Z"
                                                               fill="#757575" />
                                                        <path d="M16 8C16 9.10457 15.1046 10 14 10C12.8954 10 12 9.10457 12 8C12 6.89543 12.8954 6 14 6C15.1046 6 16 6.89543 16 8Z"
                                                               fill="#757575" />
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
import CheckBox from '../embrillons/CheckBox.vue';
export default {
       name: "AllStaff",
       components: {
              TableStepper,
              CheckBox,
       },

       data() {
              return ({
                     name: "Serhii Movchan",
                     itemSelect: false,
                     checkKey: 0,
                     items: [1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 1]
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
