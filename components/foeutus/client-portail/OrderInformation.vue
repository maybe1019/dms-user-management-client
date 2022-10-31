<template>




       <div
              class=" rounded-[4px] border-[0.5px] w-full border-gray-light min-h-[335px] p-[50px] space-y-[50px] relative sm:p-[1rem]">
              <div class=" flex flex-col justify-center items-center w-full ">

                     <div class="flex  flex-col w-full justify-center items-center max-w-[792.07px] h-[29px] ">
                            <div class=" font-roboto font-[400] text-[24px] leading-[28.13px]"> Order Information</div>
                            <p class="text-[#757575]  leading-[14.6px] text-[12px] font-[400] font-roboto ">Please enter
                                   all
                                   information</p>
                     </div>


              </div>

              <div
                     class="  flex flex-row space-x-[10px]   relative sm:flex-col sm:space-y-[10px] sm:items-center sm:space-x-0 ">
                     <!-- test -->
                     <div class="flex flex-col space-y-[20.41px]">
                            <div class=" flex space-x-[10px]">
                                   <div class="relative sm:w-full w-[267px]">
                                          <input type="text" id="parent-folder" value="Serhii Movchan" readonly
                                                 class="block px-[21px] pb-[16.75px] pt-4 w-full leading-[16.41px] text-[14px] font-[400] font-roboto  min-h-[50px]  text- text-gray-900 bg-transparent rounded-[4px] border border-[#DEE0E4] appearance-none  focus:outline-none focus:ring-0 focus:border-[#DEE0E4]"
                                                 placeholder=" " />
                                          <label for="parent-folder"
                                                 class="absolute text-[#757575]  leading-[16.41px] text-[14px] font-[400] font-roboto   duration-300 transform -translate-y-[18px] translate-x-[9px] scale-100 top-2 z-10 origin-[0] bg-white  pl-[6px] pr-[12px]   peer-focus:text-[#757575]  peer-placeholder-shown:scale-100 peer-placeholder-shown:-translate-y-1/2 peer-placeholder-shown:top-1/2 peer-focus:top-2 peer-focus:scale-100 peer-focus:-translate-y-4 left-1">
                                                 Client Name</label>
                                   </div>

                                   <div class="relative sm:w-full w-[267px]">
                                          <input type="text" id="contact-number" value="1202444" readonly
                                                 class="block px-[21px] pb-[16.75px] pt-4 w-full leading-[16.41px] text-[14px] font-[400] font-roboto  min-h-[50px]  text- text-gray-900 bg-transparent rounded-[4px] border border-[#DEE0E4] appearance-none  focus:outline-none focus:ring-0 focus:border-[#DEE0E4]"
                                                 placeholder=" " />
                                          <label for="contact-number"
                                                 class="absolute text-[#757575]  leading-[16.41px] text-[14px] font-[400] font-roboto   duration-300 transform -translate-y-[18px] translate-x-[9px] scale-100 top-2 z-10 origin-[0] bg-white  pl-[6px] pr-[12px]   peer-focus:text-[#757575]  peer-placeholder-shown:scale-100 peer-placeholder-shown:-translate-y-1/2 peer-placeholder-shown:top-1/2 peer-focus:top-2 peer-focus:scale-100 peer-focus:-translate-y-4 left-1">
                                                 Order Number</label>
                                   </div>
                            </div>
                            <div class=" flex space-x-[10px]">
                                   <div class="relative sm:w-full w-[267px]">
                                          <input type="text" id="parent-folder" value="approved" readonly
                                                 class="block px-[34px] pb-[16.75px] pt-4 w-full leading-[16.41px] text-[14px] font-[400] font-roboto  min-h-[50px]  text-green-dark bg-transparent rounded-[4px] border border-[#DEE0E4] appearance-none  focus:outline-none focus:ring-0 focus:border-[#DEE0E4]"
                                                 placeholder=" " />
                                          <label for="parent-folder"
                                                 class="absolute  text-[#757575]  leading-[16.41px] text-[14px] font-[400] font-roboto   duration-300 transform -translate-y-[18px] translate-x-[9px] scale-100 top-2 z-10 origin-[0] bg-white  pl-[6px] pr-[12px]   peer-focus:text-[#757575]  peer-placeholder-shown:scale-100 peer-placeholder-shown:-translate-y-1/2 peer-placeholder-shown:top-1/2 peer-focus:top-2 peer-focus:scale-100 peer-focus:-translate-y-4 left-1">
                                                 Status</label>

                                          <div class="w-[8px] h-[8px] bg-[#0FAA58]  absolute  origin-[0] rounded-full transform -translate-y-1/2  top-1/2 ml-[16px] " > </div>
                                   </div>

                                   <div class="relative sm:w-full w-[267px] ">
                                          <input type="datetime-local" id="dte" value="2019-12-19 09:55" readonly
                                                 class="block px-[21px] pb-[16.75px] pt-4 w-full leading-[16.41px] text-[14px] font-[400] font-roboto  min-h-[50px]  text- text-gray-900 bg-transparent rounded-[4px] border border-[#DEE0E4]   focus:outline-none focus:ring-0 focus:border-[#DEE0E4] appearance-none "
                                                 placeholder=" " />
                                          <label for="dte"
                                                 class="absolute text-[#757575]  leading-[16.41px] text-[14px] font-[400] font-roboto   duration-300 transform -translate-y-[18px] translate-x-[9px] scale-100 top-2 z-10 origin-[0] bg-white  pl-[6px] pr-[12px]   peer-focus:text-[#757575]  peer-placeholder-shown:scale-100 peer-placeholder-shown:-translate-y-1/2 peer-placeholder-shown:top-1/2 peer-focus:top-2 peer-focus:scale-100 peer-focus:-translate-y-4 left-1">
                                                 Dua Date</label>
                                   </div>
                            </div>

                     </div>
                     <!-- text area -->
                     <div class="relative sm:w-full w-[700px]">
                            <textarea id="address" readonly
                                   class="block px-[21px] pb-[16.75px] pt-4 w-full leading-[16.41px] text-[14px] font-[400] font-roboto  h-[133px]  text- text-gray-900 bg-transparent rounded-[4px] border border-[#DEE0E4] appearance-none  focus:outline-none focus:ring-0 focus:border-[#DEE0E4]"
                                   placeholder=" ">Comments about tasks</textarea>
                            <label for="address"
                                   class="absolute text-[#757575]  leading-[16.41px] text-[14px] font-[400] font-roboto   duration-300 transform -translate-y-[18px] translate-x-[9px] scale-100 top-2 z-10 origin-[0] bg-white  pl-[6px] pr-[12px]   peer-focus:text-[#757575]  peer-placeholder-shown:scale-100 peer-placeholder-shown:-translate-y-1/2 peer-placeholder-shown:top-1/2 peer-focus:top-2 peer-focus:scale-100 peer-focus:-translate-y-4 left-1">
                                   Production Information</label>
                     </div>
              </div>
       </div>
</template>
<script>

export default {
       name: "OrderInformation",

};
</script>
<style scoped>

</style>
