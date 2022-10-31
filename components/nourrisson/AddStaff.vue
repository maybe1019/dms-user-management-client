<template>
       <div class="w-full">






              <div
                     class=" fixed inset-0 z-[9999] mx-auto  my-3    w-[586px]   justify-center rounded-[4px] flex flex-col  bg-white ">


                     <div
                            class="flex items-start justify-between py-5 px-[43px] border-b border-solid shadow-sm border-slate-200 rounded-t">
                            <div class="text-[18px] font-[700] font-roboto leading-[21.09px] text-[#212121]">
                                   Add Staff
                            </div>

                     </div>
                     <div class="  w-full  flex-col space-y-[19px] mt-[41px] px-[43px]">









                            <div class=" flex  space-x-[10px] w-full ">
                                   <div
                                          class="relative h-[50px] rounded-[4px] border border-[#DEE0E4]   w-[245px] flex items-center">
                                          <input type="text" id="first-name" value="First Name"
                                                 class="block px-[21px] w-full leading-[16.41px] text-[14px] font-[400] font-roboto    text-gray-900 bg-transparent  appearance-none  focus:outline-none focus:ring-0 focus:border-[#DEE0E4] "
                                                 placeholder=" " />
                                          <label for="first-name"
                                                 class="absolute text-[#757575]  leading-[16.41px] text-[14px] font-[400] font-roboto   duration-300 transform -translate-y-[18px] translate-x-[11px] scale-100 top-2 z-10 origin-[0] bg-white  pl-[6px] pr-[4px]   peer-focus:text-[#757575]  peer-placeholder-shown:scale-100 peer-placeholder-shown:-translate-y-1/2 peer-placeholder-shown:top-1/2 peer-focus:top-2 peer-focus:scale-75 peer-focus:-translate-y-4 left-1">
                                                 First Name</label>
                                   </div>

                                   <div
                                          class="relative h-[50px] rounded-[4px] border border-[#DEE0E4]  w-[245px] flex items-center">
                                          <input type="text" id="first-name" value="Second Name"
                                                 class="block px-[21px] w-full leading-[16.41px] text-[14px] font-[400] font-roboto    text-gray-900 bg-transparent  appearance-none  focus:outline-none focus:ring-0 focus:border-[#DEE0E4] "
                                                 placeholder=" " />
                                          <label for="second-name"
                                                 class="absolute text-[#757575]  leading-[16.41px] text-[14px] font-[400] font-roboto   duration-300 transform -translate-y-[18px] translate-x-[11px] scale-100 top-2 z-10 origin-[0] bg-white  pl-[6px] pr-[4px]   peer-focus:text-[#757575]  peer-placeholder-shown:scale-100 peer-placeholder-shown:-translate-y-1/2 peer-placeholder-shown:top-1/2 peer-focus:top-2 peer-focus:scale-75 peer-focus:-translate-y-4 left-1">
                                                 Second Name</label>
                                   </div>


                            </div>



                            <FormCustomSelect :options="['Without Designation', 'python', 'rust', 'javascript']"
                                   :default="'Without Designation'" :cssClass="'w-full'" :label="'Designation'"
                                   class="select z-[9999]" />



                            <div class=" flex space-x-[10px]">

                                   <FormCustomSelect :options="['Male', 'Femele']" :default="'Male'"
                                          :cssClass="'sm:w-full w-[245px]'" :label="'Gender'" class="select z-[99]" />
                                   <div
                                          class="relative h-[50px] rounded-[4px] border border-[#DEE0E4]  w-[245px] flex items-center">
                                          <input type="text" id="date" value="2018-07-22"
                                                 class="block px-[21px] w-full leading-[16.41px] text-[14px] font-[400] font-roboto    text-gray-900 bg-transparent  appearance-none  focus:outline-none focus:ring-0 focus:border-[#DEE0E4] "
                                                 placeholder=" " />
                                          <label for="date"
                                                 class="absolute text-[#757575]  leading-[16.41px] text-[14px] font-[400] font-roboto   duration-300 transform -translate-y-[18px] translate-x-[11px] scale-100 top-2 z-10 origin-[0] bg-white  pl-[6px] pr-[4px]   peer-focus:text-[#757575]  peer-placeholder-shown:scale-100 peer-placeholder-shown:-translate-y-1/2 peer-placeholder-shown:top-1/2 peer-focus:top-2 peer-focus:scale-75 peer-focus:-translate-y-4 left-1">
                                                 Date Of Birth</label>
                                   </div>



                            </div>

                            <div
                                   class="relative h-[50px] rounded-[4px] border border-[#DEE0E4]  w-full flex items-center">
                                   <input type="email" id="email" value="biwate8033@yubua.com"
                                          class="block px-[21px] w-full leading-[16.41px] text-[14px] font-[400] font-roboto    text-gray-900 bg-transparent  appearance-none  focus:outline-none focus:ring-0 focus:border-[#DEE0E4] "
                                          placeholder=" " />
                                   <label for="email"
                                          class="absolute text-[#757575]  leading-[16.41px] text-[14px] font-[400] font-roboto   duration-300 transform -translate-y-[18px] translate-x-[11px] scale-100 top-2 z-10 origin-[0] bg-white  pl-[6px] pr-[4px]   peer-focus:text-[#757575]  peer-placeholder-shown:scale-100 peer-placeholder-shown:-translate-y-1/2 peer-placeholder-shown:top-1/2 peer-focus:top-2 peer-focus:scale-75 peer-focus:-translate-y-4 left-1">
                                          Email</label>
                            </div>

                            <div class=" flex space-x-[10px] w-full">
                                   <div
                                          class="relative h-[50px] rounded-[4px] border border-[#DEE0E4]  w-[245px]  flex items-center">
                                          <input type="text" id="parent-folder" value="Parent Folder"
                                                 class="block px-[21px] w-full leading-[16.41px] text-[14px] font-[400] font-roboto    text-gray-900 bg-transparent  appearance-none  focus:outline-none focus:ring-0 focus:border-[#DEE0E4] "
                                                 placeholder=" " />
                                          <label for="parent-folder"
                                                 class="absolute text-[#757575]  leading-[16.41px] text-[14px] font-[400] font-roboto   duration-300 transform -translate-y-[18px] translate-x-[11px] scale-100 top-2 z-10 origin-[0] bg-white  pl-[6px] pr-[4px]   peer-focus:text-[#757575]  peer-placeholder-shown:scale-100 peer-placeholder-shown:-translate-y-1/2 peer-placeholder-shown:top-1/2 peer-focus:top-2 peer-focus:scale-75 peer-focus:-translate-y-4 left-1">
                                                 Parent Folder</label>
                                   </div>
                                   <div
                                          class="relative h-[50px] rounded-[4px] border border-[#DEE0E4] w-[245px]  flex items-center">
                                          <input type="number" id="contact-number" value="1234566"
                                                 class="block px-[21px] w-full leading-[16.41px] text-[14px] font-[400] font-roboto    text-gray-900 bg-transparent  appearance-none  focus:outline-none focus:ring-0 focus:border-[#DEE0E4] "
                                                 placeholder=" " />
                                          <label for="contact-number"
                                                 class="absolute text-[#757575]  leading-[16.41px] text-[14px] font-[400] font-roboto   duration-300 transform -translate-y-[18px] translate-x-[11px] scale-100 top-2 z-10 origin-[0] bg-white  pl-[6px] pr-[4px]   peer-focus:text-[#757575]  peer-placeholder-shown:scale-100 peer-placeholder-shown:-translate-y-1/2 peer-placeholder-shown:top-1/2 peer-focus:top-2 peer-focus:scale-75 peer-focus:-translate-y-4 left-1">
                                                 Contact Number</label>
                                   </div>





                            </div>

                            <div class="relative">
                                   <textarea id="address"
                                          class="block px-[21px] pt-[17px]  w-full leading-[16.41px] text-[14px] font-[400] font-roboto  h-[100px]  text-gray-900 bg-transparent rounded-[4px] border border-[#DEE0E4] appearance-none  focus:outline-none focus:ring-0 focus:border-[#DEE0E4] "
                                          placeholder=" ">Geroev Dnipra st.57, Ukraine</textarea>
                                   <label for="address"
                                          class="absolute text-[#757575]  leading-[16.41px] text-[14px] font-[400] font-roboto   duration-300 transform -translate-y-[18px] translate-x-[11px] scale-100 top-2 z-10 origin-[0] bg-white  pl-[6px] pr-[4px]   peer-focus:text-[#757575]  peer-placeholder-shown:scale-100 peer-placeholder-shown:-translate-y-1/2 peer-placeholder-shown:top-1/2 peer-focus:top-2 peer-focus:scale-75 peer-focus:-translate-y-4 left-1">
                                          Address</label>
                            </div>



                            <div class=" flex space-x-[10px]">
                                   <div
                                          class="relative h-[50px] rounded-[4px] border border-[#DEE0E4]  w-[245px]  flex items-center">
                                          <input type="text" id="emergency-person" value="-"
                                                 class="block px-[21px] w-full leading-[16.41px] text-[14px] font-[400] font-roboto    text-gray-900 bg-transparent  appearance-none  focus:outline-none focus:ring-0 focus:border-[#DEE0E4] "
                                                 placeholder=" " />
                                          <label for="emergency-person"
                                                 class="absolute text-[#757575]  leading-[16.41px] text-[14px] font-[400] font-roboto   duration-300 transform -translate-y-[18px] translate-x-[11px] scale-100 top-2 z-10 origin-[0] bg-white  pl-[6px] pr-[4px]   peer-focus:text-[#757575]  peer-placeholder-shown:scale-100 peer-placeholder-shown:-translate-y-1/2 peer-placeholder-shown:top-1/2 peer-focus:top-2 peer-focus:scale-75 peer-focus:-translate-y-4 left-1">
                                                 Emergency Contact Person</label>
                                   </div>

                                   <div
                                          class="relative h-[50px] rounded-[4px] border border-[#DEE0E4]  w-[245px]  flex items-center">
                                          <input type="text" id="emergency-number" value="-"
                                                 class="block px-[21px] w-full leading-[16.41px] text-[14px] font-[400] font-roboto    text-gray-900 bg-transparent  appearance-none  focus:outline-none focus:ring-0 focus:border-[#DEE0E4] "
                                                 placeholder=" " />
                                          <label for="emergency-number"
                                                 class="absolute text-[#757575]  leading-[16.41px] text-[14px] font-[400] font-roboto   duration-300 transform -translate-y-[18px] translate-x-[11px] scale-100 top-2 z-10 origin-[0] bg-white  pl-[6px] pr-[4px]   peer-focus:text-[#757575]  peer-placeholder-shown:scale-100 peer-placeholder-shown:-translate-y-1/2 peer-placeholder-shown:top-1/2 peer-focus:top-2 peer-focus:scale-75 peer-focus:-translate-y-4 left-1">
                                                 Emergency Number</label>
                                   </div>


                            </div>
                            <div
                                   class="relative h-[50px] rounded-[4px] border border-[#DEE0E4]  w-full flex items-center">
                                   <input type="text" id="relationship" value="-"
                                          class="block px-[21px] w-full leading-[16.41px] text-[14px] font-[400] font-roboto    text-gray-900 bg-transparent  appearance-none  focus:outline-none focus:ring-0 focus:border-[#DEE0E4] "
                                          placeholder=" " />
                                   <label for="relationship"
                                          class="absolute text-[#757575]  leading-[16.41px] text-[14px] font-[400] font-roboto   duration-300 transform -translate-y-[18px] translate-x-[11px] scale-100 top-2 z-10 origin-[0] bg-white  pl-[6px] pr-[4px]   peer-focus:text-[#757575]  peer-placeholder-shown:scale-100 peer-placeholder-shown:-translate-y-1/2 peer-placeholder-shown:top-1/2 peer-focus:top-2 peer-focus:scale-75 peer-focus:-translate-y-4 left-1">
                                          Relationship</label>
                            </div>









                     </div>


                     <div class=" flex items-center justify-center space-x-[10px] mt-[47px] mb-[65px] ">
                            <button class=" text-center w-full max-w-[200px] h-[50px]  border border-[#DEE0E4] font-medium  bg-white  font-roboto  text-[14px] text-[#757575] rounded-[4px] outline-none focus:outline-none  mb-1 ease-linear transition-all duration-150"
                                   type="button" @click="toggleModal(1)">
                                   Back
                            </button>
                            <button class=" text-center w-full max-w-[200px] h-[50px]  font-medium bg-[#4489FE]   font-roboto  text-[14px] text-[#FFFFFF] rounded-[4px] outline-none focus:outline-none mb-1 ease-linear transition-all duration-150"
                                   type="button" @click="toggleModal(1)">
                                   Add Staff
                            </button>
                     </div>



              </div>
              <div v-show="showModal" class="opacity-20 fixed inset-0 z-40 bg-black-dark"></div>
       </div>
</template>

<script>
import FormCustomSelect from '../embrillons/FormCustomSelect.vue';
export default {
       emits: ['addAction'],
       components: {
              FormCustomSelect
       },

       name: "AddStaff",
       data() {
              return {
                     showModal: true
              }
       },
       methods: {
              toggleModal: function (option) {

                     this.$emit('addAction', option)
              }
       }
}
</script>