<template>
    <div>
        <ActivityHeaderFilter :title="'Last Activity'" />

        <table class="w-full border-collapse   text-left mt-[57px] ">
            <thead class="  ">
                <tr class="border-none leading-[14.46px] text-[#212121] text-[12px] font-roboto font-medium">


                    <th scope="col" class="py-3 pb-[20.75px]  !pl-[35px]  w-[314px]">
                        Type
                    </th>
                    <th scope="col" class="py-3 pb-[20.75px] w-[342px]">
                        Time
                    </th>
                    <th scope="col" class="py-3 pb-[20.75px] w-[544px] ">
                        Last Activity
                    </th>
                   


                </tr>
            </thead>

            <tbody class="leading-[16.41px] text-[#212121] text-[14px] font-roboto font-[400]">
                <tr class="  hover:bg-gray-50 h-[91.5px]">




                    <td class="py-0 w-[314px] !pl-[35px]">
                        
                            <div
                                class=" flex leading-[14.06px] text-[12px] justify-center items-center  w-[78.32px] h-[24px] bg-green-bgsuccess text-[#0FAA58] rounded-[2px] ">
                                Payments
                            </div>
                        

                    </td>
                    <td class="py-0  w-[342px]  text-[#757575]">
                        
                            Yesterday at 6:56 PM

                        
                    </td>
                    <td class=" py-0  w-[544px]">
                        
                            <div class="flex  flex-col   items-start">
                                <div>
                                    Paymetns #1231423</div>

                                <div class="text-[#757575]">
                                    New file added in task <span class="text-blue-dark underline"> #2424525 </span> by Serhii Movchan
                                </div>
                            </div>
                       


                    </td>
                    


                </tr>










            </tbody>
        </table>




    </div>
</template>

<script>
import ActivityHeaderFilter from './ActivityHeaderFilter.vue'
export default {
    name: 'LastActivity',
    components: {
        ActivityHeaderFilter
    }
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
</style>
