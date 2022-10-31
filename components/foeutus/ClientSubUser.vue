<template>
    <div class="bg-wihte mt-[28px] mx-auto  w-full max-w-[814.24px] sm:w-full">
        <!-- header permission -->
        <div class=" flex justify-between items-center flex-row space-x-[5px]">
            <div class="flex items-center space-x-[30px]">
                <p class="font-roboto font-[400] text-[24px] leading-[28.13px] text-[#212121]">Sub Users</p>
                <button
                    class=" text-center w-[156px] h-[50px]   bg-[#4489FE]  font-[500] font-roboto  text-[14px] text-[#FFFFFF] rounded-[4px] outline-none focus:outline-none  ease-linear transition-all duration-150 sm:max-w-[150px] "
                    type="button">
                    Invite Sub User
                </button>


            </div>





            <FormCustomSelect :options="['John Doe (Manager)', 'Doe (Manager)']" :default="'John Doe (Manager)'"
                :cssClass="'w-full  max-w-[328px]'" :label="'Sub User Name'" class="select z-[9999]" />



        </div>

        <!-- tab permission content -->

        <table class="w-full text-sm border-collapse mt-[55px]   text-left text-gray-500  ">
            <thead class=" ">
                <tr class="border-none  leading-[14.06px] text-[#212121] text-[12px] font-roboto font-medium">

                    <th scope="col" class="py-[24.5px] !pl-[15px] w-[205px] ">
                        Page Name
                    </th>
                    <th scope="col" class="py-[24.5px] w-[110.2px]">
                        View
                    </th>
                    <th scope="col" class="py-[24.5px] w-[110.19px]">
                        Use
                    </th>
                    <th scope="col" class="py-[24.5px] w-[110.62px]">
                        Create
                    </th>
                    <th scope="col" class="py-[24.5px] w-[111px]">
                        Edit
                    </th>
                    <th scope="col" class="py-[24.5px] w-[110.24px]">
                        Delete
                    </th>
                    <th scope="col" class="py-[24.5px] w-[57.24px]">
                        All
                    </th>
                </tr>
            </thead>

            <tbody>
                

                <tr class=" hover:bg-gray-50 h-[59.5px]">

                    <td class=" border-l-0 py-0 !pl-[15px] w-[205px]  text-[#212121] font-roboto font-[400] leading-[16.41px]">
                        Prodaction
                    </td>
                    <td class="py-0 w-[110.2px]">
                        
                            <CheckBox :checkType="'determinate'" :checked="true" />

                    

                    </td>

                    <td class="py-0 w-[110.19px]">
                        
                            <CheckBox :checkType="'determinate'" :checked="true" />

                        

                    </td>
                    <td class="py-0 w-[110.62px]">
                        
                            <CheckBox :checkType="'determinate'"  :checked="true"/>

                        

                    </td>
                    <td class="py-0 w-[111px]">
                        
                            <CheckBox :checkType="'determinate'" />

                    

                    </td>

                    <td class="py-0  w-[110px]">
                        
                            <CheckBox :checkType="'determinate'" />

                        

                    </td>
                    <td class=" w-[57.24px] border-r-0">
                        
                            <CheckBox :checkType="'determinate'" />

                        

                    </td>

                </tr>
                



            </tbody>
        </table>


        <div class=" flex  items-center justify-center space-x-[10px] mt-[84px] mb-[84px] ">
            <button
                class=" text-center w-[200px] h-[50px]  border border-[#DEE0E4] font-medium  bg-white   font-roboto text-[14px] text-[#757575] rounded-[4px] outline-none focus:outline-none mr-1 mb-1 ease-linear transition-all duration-150"
                type="button">
                Cancel
            </button>
            <button
                class=" text-center w-[200px] h-[50px]   font-medium bg-[#4489FE]  font-roboto  text-[14px] text-[#FFFFFF] rounded-[4px] outline-none focus:outline-none mr-1 mb-1 ease-linear transition-all duration-150"
                type="button">
                Save Changes
            </button>
        </div>







    </div>
</template>

<script>
import CheckBox from '../embrillons/CheckBox.vue';
import FormCustomSelect from '../embrillons/FormCustomSelect.vue';
export default {
    name: "ClientSubUser",
    components: {
        FormCustomSelect,
        CheckBox
    }
};
</script>

<style scoped>
    tr th,
tr td {
    padding-right: 0px;
    padding-left: 0px;

}
</style>
