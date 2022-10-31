<template>
       <div class="font-roboto">
              <div v-show="showAddStaff">
                     <AddDesignation @addAction="displayAddStaff" />
              </div>




              <div class="flex justify-between items-center mt-[87px] w-full sm:flex-wrap">
                     <div class="font-[400] text-[24px]  loading-">Designations List
                     </div>
                     <div class="flex">


                            <button type="button" v-on:click="displayAddStaff"
                                   class="  text-[14px] text-white bg-[#4489FE]  mr-[12.5px] rounded-[4px] h-[44px]  w-[183px] sm:max-w-[183px] hover:bg-blue-700  px-2    focus:outline-none sm:w-full">
                                  <span class="font-[500]">Add Designation</span> 
                            </button>
                            <div class=" mr-[20px]">



                                   <div
                                          class="flex flex-row justify-between border border-gray-300 bg-gray-50 w-[285px] sm:w-full h-[44px] rounded-[4px] search-container">
                                          <div class="relative w-full">
                                                 <label for="search-staff">
                                                        <div
                                                               class="flex absolute inset-y-0 left-0 items-center pl-[16.41px] cursor-pointer">
                                                               <svg height="20px" viewBox="0 0 48 48" fill="#757575"
                                                                      width="20px" xmlns="http://www.w3.org/2000/svg"
                                                                      stroke="none" stroke-width="2">
                                                                      <path
                                                                             d="M31 28h-1.59l-.55-.55c1.96-2.27 3.14-5.22 3.14-8.45 0-7.18-5.82-13-13-13s-13 5.82-13 13 5.82 13 13 13c3.23 0 6.18-1.18 8.45-3.13l.55.55v1.58l10 9.98 2.98-2.98-9.98-10zm-12 0c-4.97 0-9-4.03-9-9s4.03-9 9-9 9 4.03 9 9-4.03 9-9 9z" />
                                                                      <path d="M0 0h48v48h-48z" fill="none" />
                                                               </svg>
                                                        </div>
                                                 </label>

                                                 <input type="text" id="search-staff"
                                                        class="bg-white h-full w-full text-[14px]  text-black-dark leading-[16.41px] rounded-[4px] focus:outline-none block pl-[47.33px] "
                                                        placeholder="Search" />
                                          </div>
                                   </div>
                            </div>
                            <div class="flex items-center space-x-[18.5px]">
                                   <div class="flex items-center space-x-[8.5px]">
                                          <div class="font-[400] text-[14px] leading-[16.41px] text-gray-dark "
                                                 data-dropdown-toggle="filter">
                                                 Filter
                                          </div>

                                          <div class="icon cursor-pointer h-[10px] w-[15px]" id="dropdownBottomButton"
                                                 data-dropdown-toggle="dropdownBottom" data-dropdown-placement="bottom">

                                                 <svg viewBox="0 0 48 48" xmlns="http://www.w3.org/2000/svg">
                                                        <path d="M6 36h12v-4h-12v4zm0-24v4h36v-4h-36zm0 14h24v-4h-24v4z"
                                                               fill="#757575" />
                                                        <path d="M0 0h48v48h-48z" fill="none" />
                                                 </svg>
                                          </div>
                                          
                                   </div>
                                   <div class="flex items-center space-x-[8.5px]">
                                          <div class="font-[400] text-[14px] leading-[16.41px] text-gray-dark">
                                                 Sort
                                          </div>

                                          <div class="icon cursor-pointer h-[10px] w-[15px]" id="dropdownBottomButton"
                                                 data-dropdown-toggle="dropdownBottom" data-dropdown-placement="bottom">

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


              <div id="dropdownBottom" class="hidden z-[9999]  rounded divide-y divide-gray-100 ">
                     <FilterItemBox class=" transform -translate-x-60  " />
              </div>

              <table class="w-full  border-collapse   text-left  mt-[91.75px] ">

                     <thead class=" ">
                            <tr class="bg-white  border-b leading-[14.46px] text-[#212121] text-[12px]  font-medium  " >
                                   <th scope="col" class="w-[68px] !pl-[21.37px] pb-[18.75px] pt-[40px]  bg-white">
                                          <CheckBox :checkType="'indeterminate'" :checked="true"
                                                 @selectAll="setSelectAll" />
                                   </th>

                                   <th scope="col" class=" pb-[18.75px] w-[126px] bg-white pt-[40px]  ">
                                          #
                                   </th>
                                   <th scope="col" class="pb-[18.75px] w-[291px] bg-white pt-[40px] ">
                                          Designation
                                   </th>
                                   <th scope="col" class="pb-[18.75px] w-[398px] bg-white pt-[40px] ">
                                          Role
                                   </th>
                                   <th scope="col" class="pb-[18.75px] w-[252px] bg-white pt-[40px] ">
                                          Staff Amount

                                   </th>
                                   <th scope="col" class="pb-[18.75px] w-[65px] bg-white pt-[40px]  ">
                                          Actions </th>

                            </tr>
                     </thead>


                     <tbody>
                            <tr v-for="(item, index) in items"
                                   class=" h-[91.5px] hover:bg-gray-50  py-0 leading-[16.41px] text-[#212121] text-[14px]  font-[400] pl-[21.37px] pr-[23px]"
                                   :key="index">
                                   <td class="!pl-[21.37px] w-[68px] py-0">
                                          <CheckBox :checkType="'determinate'" :checked="itemSelect" :key="checkKey" />

                                   </td>
                                   <td class=" w-[126px]  ">
                                          1
                                   </td>
                                   <td class="w-[291px]">
                                          Spanish Transcriptionist
                                   </td>

                                   <td class=" w-[398px] ">
                                          Spanish Transcriptionist
                                   </td>
                                   <td class="w-[252px]">

                                          12

                                   </td>

                                   <td class=" py-0 w-[65px] ">
                                          <div class="flex justify-end  w-[38px]">
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
       </div>
</template>

<script>
import CheckBox from '../../embrillons/CheckBox.vue';
import FilterItemBox from '../FilterItemBox.vue';
import SortFilter from '../../embrillons/SortFilter.vue';
import AddStaff from '../../nourrisson/AddStaff.vue';
import InviteStaff from '../../nourrisson/InviteStaff.vue';
import AddDesignation from './AddDesignation.vue';
export default {
       name: "FilterHeader",
       components: {
              AddStaff,
              InviteStaff,
              AddDesignation,
              SortFilter,
              FilterItemBox,
              CheckBox

       },
       data() {
              return {
                     showAddStaff: false,
                     showInViteStaff: false,
                     showFilterOption: false,
                     items: [1, 1, 1],
                     itemSelect: false,
                     checkKey: 0,

              }
       },
       methods: {
              displayAddStaff() {
                     this.showAddStaff = !this.showAddStaff
              },
              displayInviteStaff() {
                     this.showInViteStaff = !this.showInViteStaff
              },
              displayFilterOption() {
                     this.showFilterOption = !this.showFilterOption
              },
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


.icon {
       width: 20px;
       height: 20px;
       color: #757575;
}



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
