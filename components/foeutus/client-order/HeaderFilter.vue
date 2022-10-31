<template>
       <div class="font-roboto">

              <div v-show="showAddOrder">
                     <AddOrder @addAction="displayAddStaff" />
              </div>




              <div class="flex justify-between items-center mt-[87px]">
                     <div class="text-[24px] leading-[28.13px]  ">Orders List
                     </div>
                     <div class="flex ">


                            <button type="button" v-on:click="displayAddStaff"
                                   class="text-white font-roboto border  bg-[#4489FE] border-[#4489FE]  rounded-[4px]   w-[183px] hover:bg-blue-800 focus:ring-4 focus:ring-blue-300 font-medium  px-5 py-2.5  mb-2  focus:outline-none ">
                                   New Order
                            </button>
                            <div
                                   class="relative flex flex-row justify-between border border-gray-300 bg-gray-50 ml-[12px] mr-[20px] w-[285px] sm:w-full h-[44px] rounded-[4px] ">
                                   <label for="search-staff">
                                          <div class="flex absolute inset-y-0 left-0 items-center pl-3 cursor-pointer">

                                                 <svg height="20px" viewBox="0 0 48 48" fill="#757575" width="20px"
                                                        xmlns="http://www.w3.org/2000/svg" stroke="none"
                                                        stroke-width="2">
                                                        <path
                                                               d="M31 28h-1.59l-.55-.55c1.96-2.27 3.14-5.22 3.14-8.45 0-7.18-5.82-13-13-13s-13 5.82-13 13 5.82 13 13 13c3.23 0 6.18-1.18 8.45-3.13l.55.55v1.58l10 9.98 2.98-2.98-9.98-10zm-12 0c-4.97 0-9-4.03-9-9s4.03-9 9-9 9 4.03 9 9-4.03 9-9 9z" />
                                                        <path d="M0 0h48v48h-48z" fill="none" />
                                                 </svg>

                                          </div>
                                   </label>

                                   <input type="text" id="search-staff"
                                          class="bg-white   text-gray-dark rounded-[4px] focus:outline-none block pl-[40px] p-2.5 h-full  w-full text-[14px] leading-[16.41px] "
                                          placeholder="Search" />

                            </div>

                            <!-- filter -->
                            <div class=" space-x-[18.5px] flex">

                                   <!-- filter -->
                                   <div class="flex items-center space-x-[8.5px]">
                                          <div class="font-[400] text-[14px] leading-[16.41px] text-[#757575]"
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
                                          <!-- <div  id="filter">
                                    <FilterItemBox @filterAction="displayFilterOption" />
                             </div> -->
                                   </div>
                                   <div class="flex items-center space-x-[8.5px]">
                                          <div class="font-[400] text-[14px] leading-[16.41px] text-[#757575] ">
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



       </div>
</template>

<script>
import AddOrder from './AddOrder.vue';
import InviteStaff from './../../nourrisson/InviteStaff.vue';
export default {
       name: "HeaderFilter",
       components: {

              InviteStaff,
              AddOrder

       },
       data() {
              return {
                     showAddOrder: false,
                     showInViteStaff: false,
                     showFilterOption: false
              }
       },
       methods: {
              displayAddStaff() {
                     this.showAddOrder = !this.showAddOrder
              },
              displayInviteStaff() {
                     this.showInViteStaff = !this.showInViteStaff
              },
              displayFilterOption() {
                     this.showFilterOption = !this.showFilterOption
              }



       }




};
</script>

<style scoped>
.search-input {
       height: 100%;
       width: 100%;
       font-size: 14px;
       color: rgba(117, 117, 117, 1);
       line-height: 16.41px;
}

.icon {
       width: 20px;
       height: 20px;
       color: #757575;
}
</style>
