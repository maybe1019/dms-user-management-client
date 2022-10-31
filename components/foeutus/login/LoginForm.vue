<template>
       <div class=" w-full max-w-[450px] ">
              <div class=" w-full  inset-0 z-50    outline-none">
                     <div class="relative  w-full ">
                            <!--content-->
                            <div
                                   class=" rounded-[4px]  relative flex flex-col w-full bg-white outline-none focus:outline-none">
                                   <!--header-->

                                   <!--body-->
                                   <div class="relative flex flex-col justify-start  space-y-[39px]  w-full">
                                          <div class="space-y-[18px]">
                                                 <div
                                                        class="text-[24px] font-[400] font-roboto leading-[21.09px] text-[#212121]">
                                                        Sign in to DeskVantage
                                                 </div>
                                                 <div
                                                        class="text-gray-dark text-[14px] font-[400] font-roboto leading-[16.41px] ">
                                                        Enter your details below
                                                 </div>

                                          </div>

                                          <div class="space-y-[26px]  w-full">
                                                 <div class="relative  w-full flex">
                                                        <input type="email" id="email" value="biwate8033@yubua.com"
                                                               class="block px-[21px]  w-full leading-[16.41px] text-[14px] font-[400] font-roboto  h-[50px]  text- text-gray-900 bg-transparent rounded-l-[4px] border border-[#DEE0E4] appearance-none focus:outline-none focus:ring-0 focus:border-[#DEE0E4] "
                                                               placeholder=" " />
                                                        <label for="email"
                                                               class="  absolute text-[#757575]  leading-[16.41px] text-[14px] font-[400] font-roboto   duration-300 transform -translate-y-[18px] translate-x-[9px] scale-100 top-2 z-10 origin-[0] bg-white  pl-[6px] pr-[12px]   peer-focus:text-[#757575]  peer-placeholder-shown:scale-100 peer-placeholder-shown:-translate-y-1/2 peer-placeholder-shown:top-1/2 peer-focus:top-2 peer-focus:scale-75 peer-focus:-translate-y-4 left-1">
                                                               Email</label>


                                                        <FormCustomSelect
                                                               :options="['Client', 'Staff', 'Admin', 'Reseller']"
                                                               :default="'Reseller'" :cssClass="'w-full max-w-[103px]'"
                                                               :selectCss="'!bg-[#DEE0E4] !rounded-l-none '" 
                                                               class=" select z-[100]" />

                                                 </div>
                                                 <div class="relative  w-full">
                                                        <input type="text" id="password"  v-on:input="putStart()" v-model="password"
                                                               
                                                               class="block px-[21px] w-full leading-[16.41px] text-[14px] font-[400] font-roboto  h-[50px]  text- text-gray-900 bg-transparent rounded-[4px] border border-[#DEE0E4] appearance-none focus:outline-none focus:ring-0 focus:border-[#DEE0E4] "
                                                               placeholder=" " />
                                                        <label for="password"
                                                               class="absolute text-[#757575]  leading-[16.41px] text-[14px] font-[400] font-roboto   duration-300 transform -translate-y-[18px] translate-x-[11px] scale-100 top-2 z-10 origin-[0] bg-white  pl-[6px] pr-[4px]   peer-focus:text-[#757575]  peer-placeholder-shown:scale-100 peer-placeholder-shown:-translate-y-1/2 peer-placeholder-shown:top-1/2 peer-focus:top-2 peer-focus:scale-75 peer-focus:-translate-y-4 left-1">
                                                               Password</label>
                                                 </div>
                                                 <!-- remember me -->

                                          </div>



                                   </div>



                                   <div class=" flex justify-between items-center mt-[12px] ">
                                          <div class="flex items-center space-x-[10px]">

                                                 <LoginCheckbox :checked="true" id="muhRadio" />
                                                 <label for="muhRadio"
                                                        class="text-black-dark  leading-[15.23px] text-[13px] font-[400] font-roboto">


                                                        Remember
                                                        me
                                                 </label>
                                          </div>
                                          <a herf=""
                                                 class=" underline cursor-pointer text-[#757575]  leading-[15.23px] text-[13px] font-[400] font-roboto ">Forgot
                                                 Password?</a>
                                   </div>


                                   <div class="w-full flex items-center justify-center space-x-[10px] mt-[54px]">

                                          <button class="  text-center w-full h-[44px]   font-medium bg-[#4489FE]   font-roboto  text-[14px] text-[#FFFFFF] rounded-[4px] outline-none focus:outline-none ease-linear transition-all duration-150"
                                                 type="button">
                                                 Sign In
                                          </button>
                                   </div>
                                   <div class=" leading-[16.41px] text-[14px] font-medium font-roboto mt-[25px] w-full flex justify-center">
                                          <span>Don't have an account?  </span> &nbsp;<a href="" class="underline text-blue-dark">Create new
                                                 one</a>
                                   </div>
                                   <!--footer-->

                            </div>
                     </div>
              </div>
       </div>
</template>
<script>
import LoginCheckbox from './LoginCheckbox.vue';
import CheckBox from '../../embrillons/CheckBox.vue';
import FormCustomSelect from '../../embrillons/FormCustomSelect.vue';
export default {
       name: "LoginFrom",
       components: { FormCustomSelect, CheckBox, LoginCheckbox },
       data() {
              return {
                     password:"***************"
              }
       },
       methods: {
              putStart() {
                     let newPass =""
                     for (let index = 0; index < this.password.length; index++) {
                          newPass= newPass+  "*"
                            // console.log('mot de passe',this.password[index])
                            
                     }
                     this.password = newPass
              }
              
       }
};
</script>
<style scoped>

</style>
