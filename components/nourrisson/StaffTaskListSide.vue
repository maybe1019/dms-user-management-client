<template>
       <div class="w-[500px] py-5 space-y-[45px] flex flex-col sm:w-full">
              <!-- header -->
              <div class="flex flex-row justify-between items-center">
                     <div class="flex flex-row justify-between items-center space-x-[18.5px] font-roboto">
                            <div class="font-roboto leading-[25.78px] font-[400] text-[22px]">
                                   Tasks
                            </div>
                            <div class="flex items-center space-x-[8.5px]">
                                   <div class="font-roboto text-[14px] leading-[16.41px] font-[400] text-[#757575]">
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
                                   <span class="font-roboto text-[14px] leading-[16.41px] font-[400] text-[#757575]">
                                          Sort
                                   </span>

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
                     <!-- linl to all projects -->
                     <div>
                            <a href="/staff"
                                   class="font-[400] underline text-[#4489FE] text-[14px] leading-[16.41px] float-right font-roboto">
                                   All Tasks
                            </a>
                     </div>
              </div>
              <!-- list -->
              <div>
                     <div class="overflow-x-auto relative sm:rounded-lg">
                            <table class="border-collapse w-full  text-left text-gray-500">
                                   <thead class="text-[12px] text-[#212121] font-medium font-roboto border-b">
                                          <tr>
                                                 <th scope="col" class="py-[20.05px] w-[250px]">Task Name</th>
                                                 <th scope="col" class="py-[20.05px] w-[163px]">status</th>
                                                 <th scope="col" class="py-[20.05px] w-[87px]  ">Staff</th>
                                          </tr>
                                   </thead>
                                   <tbody>
                                          <tr class="bg-white h-[53.5px]">
                                                 <td scope="row"
                                                        class="py-0 w-[250px] font-[400] text-[14px] leading-[16.41px] text-[#212121] font-roboto ">
                                                        <div class="flex">
                                                               <span>English Task</span>
                                                               <span class="ml-[11px]">
                                                                      <svg xmlns="http://www.w3.org/2000/svg"
                                                                             class="h-[15px] w-[15px] text-[#4489fe] cursor-pointer"
                                                                             fill="none" viewBox="0 0 24 24"
                                                                             stroke="currentColor" stroke-width="2">
                                                                             <path stroke-linecap="round"
                                                                                    stroke-linejoin="round"
                                                                                    d="M10 6H6a2 2 0 00-2 2v10a2 2 0 002 2h10a2 2 0 002-2v-4M14 4h6m0 0v6m0-6L10 14" />
                                                                      </svg>
                                                               </span>
                                                        </div>
                                                 </td>
                                                 <td class="py-0 w-[163px]">

                                                        <div
                                                               class="flex items-center leading-[15.23px] text-blue-dark text-[13px] font-roboto font-[400]">
                                                               <div
                                                                      class="h-[6px] w-[6px]  rounded-full bg-blue-dark mr-[8px]">
                                                               </div>
                                                               in Production
                                                        </div>

                                                 </td>
                                                 <td class="py-0 w-[87px] !pr">

                                                        <div class="flex -space-x-[16px]   flex-none">
                                                               <img class="w-[32.63px] h-[32.63px] rounded-full border-[3px] border-white"
                                                                      src="profil.jpeg" alt="" />
                                                               <img class="w-[32.63px] h-[32.63px] rounded-full border-[3px] border-white"
                                                                      src="profil.jpeg" alt="" />
                                                               <img class="w-[32.63px] h-[32.63px] rounded-full border-[3px] border-white"
                                                                      src="profil.jpeg" alt="" />
                                                               <a class="flex justify-center items-center w-[32.63px] h-[32.63px] text-[12px] font-medium text-[#818181] bg-[#DBDBDB] rounded-full border-[2px] border-white hover:bg-gray-600"
                                                                      href="#">
                                                                      +5
                                                               </a>
                                                        </div>


                                                 </td>
                                          </tr>


                                   </tbody>
                            </table>
                     </div>
              </div>
       </div>
</template>

<script>
export default {
       name: 'StaffTaskListSide',
}
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







.icon {
       width: 20px;
       height: 20px;
       color: #757575;
}
</style>
