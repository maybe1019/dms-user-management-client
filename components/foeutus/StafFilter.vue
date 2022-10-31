<template>
  <div class="font-roboto w-full">
    <div v-show="showAddStaff">
      <AddStaff @addAction="displayAddStaff" />
    </div>

    <div v-show="showInViteStaff">
      <InviteStaff @addAction="displayInviteStaff" />
    </div>

    <div class="flex justify-between items-center mt-[87px] sm:flex-wrap">
      <div class="text-[24px] leading-[28.13px]">Staff List</div>
      <div class="flex">
        <div class="flex space-x-[6px]">
          <div class="  h-[44px]">
            <button type="button" v-on:click="displayInviteStaff"
              class=" inline-block text-[#4489FE]  bg-white border border-[#4489FE] rounded-[4px] w-[183px] sm:max-w-[183px]  h-full hover:bg-gray-100 font-medium ">

              <p class="text-[14px]">Invite Staff</p>
            </button>
          </div>
          <div class="w-full max-w-[183px]  h-[44px]">
            <button type="button" v-on:click="displayAddStaff"
              class="  bg-[#4489FE] text-[14px] border-[#4489FE] text-[#FFFFFF] rounded-[4px]  w-[183px] sm:max-w-[183px]  leading-[16.41px] h-full  hover:bg-blue-400 font-medium ">
              <p>Add Staff</p>
            </button>
          </div>
        </div>




        <div
          class="relative flex flex-row justify-between border border-gray-300 bg-gray-50 ml-[12px] mr-[20px] w-[285px] sm:w-full h-[44px] rounded-[4px] ">
          <label for="search-staff">
            <div class="flex absolute inset-y-0 left-0 items-center pl-3 cursor-pointer">
             

              <svg height="20px" viewBox="0 0 48 48" fill="#757575" width="20px" xmlns="http://www.w3.org/2000/svg" stroke="none" stroke-width="2">
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

        <div class=" space-x-[18.5px] flex">

          <!-- filter -->
          <div class="flex items-center space-x-[8.5px]">
            <div class="font-[400] text-[14px] leading-[16.41px] text-[#757575]" data-dropdown-toggle="filter">
              Filter
            </div>

            <div class="icon cursor-pointer h-[10px] w-[15px]" id="dropdownBottomButton"
              data-dropdown-toggle="dropdownBottom" data-dropdown-placement="bottom">

              <svg viewBox="0 0 48 48" xmlns="http://www.w3.org/2000/svg">
                <path d="M6 36h12v-4h-12v4zm0-24v4h36v-4h-36zm0 14h24v-4h-24v4z" fill="#757575" />
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

              <!-- <svg  viewBox="0 0 48 48"  xmlns="http://www.w3.org/2000/svg">
              <path d="M6 36h12v-4h-12v4zm0-24v4h36v-4h-36zm0 14h24v-4h-24v4z" fill="#757575" />
              <path d="M0 0h48v48h-48z" fill="none"  />
            </svg> -->

              <svg viewBox="0 0 48 48" xmlns="http://www.w3.org/2000/svg">
                <path d="M6 36h12v-4h-12v4zm0-24v4h36v-4h-36zm0 14h24v-4h-24v4z" fill="#757575" />
                <path d="M0 0h48v48h-48z" fill="none" />
              </svg>
            </div>


          </div>

        </div>


      </div>
    </div>

    <!-- filter toogle options -->
    <div class="flex justify-end items-center mt-[16px] mr-[60px]">
      <div class="flex space-x-[6px]">
        <div
          class="border-0 bg-[#E9F0FD] py-[5.83] px-[9px] h-[28px] space-x-[9.82px] flex items-center rounded-[4px]">
          <span class=" font-[400] text-[12px] center leading-[14.06px] text-[#4489FE]">
            Proofreader
          </span>

          <svg xmlns="http://www.w3.org/2000/svg" class="h-[15px] w-[15px] stroke-[#4489FE] cursor-pointer" fill="none"
            viewBox="0 0 24 24" stroke="currentColor" stroke-width="2">
            <path stroke-linecap="round" stroke-linejoin="round" d="M6 18L18 6M6 6l12 12" />
          </svg>
        </div>
        <div
          class="border-0 bg-[#E9F0FD] py-[5.83] px-[9px] h-[28px] space-x-[9.82px] flex items-center rounded-[4px]">
          <span class=" font-[400] text-[12px] center leading-[14.06px] text-[#4489FE]">
            Without Tasks
          </span>

          <svg xmlns="http://www.w3.org/2000/svg" class="h-[15px] w-[15px] stroke-[#4489FE] cursor-pointer" fill="none"
            viewBox="0 0 24 24" stroke="currentColor" stroke-width="2">
            <path stroke-linecap="round" stroke-linejoin="round" d="M6 18L18 6M6 6l12 12" />
          </svg>
        </div>
      </div>
      <div class="ml-[20px]  cursor-pointer font-[400] text-[14px] leading-[16.41px] text-[#4489FE] underline">
        Clear Filter
      </div>
    </div>



    <!-- Dropdown menu filter-->
    <div id="dropdownBottom" class="hidden z-[9999]  rounded divide-y divide-gray-100 ">
      <FilterItemBox @filterAction="displayFilterOption" class=" transform -translate-x-60  " />
    </div>
  </div>
</template>

<script>
import AddStaff from '../nourrisson/AddStaff.vue'
import InviteStaff from '../nourrisson/InviteStaff.vue'
import FilterItemBox from '../nourrisson/FilterItemBox.vue'
export default {
  name: 'StafFilter',
  components: {
    AddStaff,
    InviteStaff,
    FilterItemBox,
  },
  data() {
    return {
      showAddStaff: false,
      showInViteStaff: false,
      showFilterOption: false,
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
  },
}
</script>

<style scoped>
.icon {
  width: 20px;
  height: 20px;
  color: #757575;
}

.text-filters {
  font-size: 14px;
  font-weight: 400;
  line-height: 16.41px;
  color: #757575;
}
</style>
