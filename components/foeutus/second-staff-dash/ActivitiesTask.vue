<template>
  <div>
    <ActivityHeaderFilter :title="'My Active Task'" />

    <table class="w-full border-collapse   text-left mt-[57px] ">
      <thead class="  ">
        <tr class="border-none leading-[14.46px] text-[#212121] text-[12px] font-roboto font-medium">


          <th scope="col" class="py-3 pb-[19.75px] !pl-[30px] w-[313px] ">
            Task Name
          </th>
          <th scope="col" class="py-3 pb-[19.75px] w-[176px]">
            Last Activity
          </th>
          <th scope="col" class="py-3 pb-[19.75px] w-[486px]">
            Descriprion
          </th>
          <th scope="col" class="py-3 pb-[19.75px]">

          </th>


        </tr>
      </thead>
      <tbody class="leading-[16.41px] text-[#212121] text-[14px] font-roboto font-[400]">
        <tr class="  hover:bg-gray-50 h-[91.5px] ">

          <td class="py-0 !pl-[30px] w-[313px] ">
         
              Task Name Number 1
        

          </td>
          <td class="py-0 w-[176px]">
           

              <div class=" space-y-[3px] text-[#757575] flex flex-col">
                <span>08/24/2019</span>
                <span> 02:30 PM</span>
              </div>
            
          </td>
          <td class="py-0  w-[486px] ">
       

              <span class=" flex items-center text-ellipsis overflow-hidden  max-w-[353px]  text-gray-dark">
                One morning, when Gregor Samsa woke from troubled dreams, he found himself transformed in his bed into a
                horrible vermin. He lay on his armour-like back,
              </span>

          

          </td>
          <td class="py-0  ">
            <div class="flex items-center space-x-[5.37px] justify-end ">

              <button type="button"
                class="text-blue-dark font-roboto bg-white border h-[36px] border-[#4489FE] rounded-[2px] w-[109.82px]  hover:bg-gray-100 font-medium px-5 py-2.5  focus:outline-none">
                View
              </button>

              <button type="button"
                class="text-white font-roboto border h-[36px] bg-[#4489FE] border-[#4489FE] rounded-[2px] w-[109.82px] hover:bg-blue-800 focus:ring-4 focus:ring-blue-300 font-medium px-5 py-2.5 focus:outline-none">
                Accept
              </button>
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
  name: 'ActivittTask',
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
