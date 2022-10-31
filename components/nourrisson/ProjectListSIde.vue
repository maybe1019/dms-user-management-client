<template>
    <div class="w-[500px] py-5 space-y-[46.5px] flex flex-col sm:max-w-[500px]">
        <!-- header -->
        <div class="flex flex-row justify-between items-center">
            <div class="flex flex-row justify-between items-center space-x-[18.5px] font-roboto">
                <div class=" font-roboto  leading-[25.78px] font-[400] text-[22px]">Projects</div>
                <div class="flex items-center space-x-[8.5px]">
                    <div class="font-roboto text-[14px] leading-[16.41px] font-[400] text-[#757575]">Filter</div>

                    <div class="icon cursor-pointer w-[20px] h-[20px] " id="dropdownBottomButton"
                        data-dropdown-toggle="dropdownBottom" data-dropdown-placement="bottom">

                        <svg viewBox="0 0 48 48" xmlns="http://www.w3.org/2000/svg">
                            <path d="M6 36h12v-4h-12v4zm0-24v4h36v-4h-36zm0 14h24v-4h-24v4z" fill="#757575" />
                            <path d="M0 0h48v48h-48z" fill="none" />
                        </svg>
                    </div>
                </div>
                <div class="flex items-center space-x-[8.5px]">
                    <span class="font-roboto text-[14px] leading-[16.41px] font-[400] text-[#757575]">Sort</span>


                    <div class="icon cursor-pointer w-[20px] h-[20px]" id="dropdownBottomButton"
                        data-dropdown-toggle="dropdownBottom" data-dropdown-placement="bottom">

                        <svg viewBox="0 0 48 48" xmlns="http://www.w3.org/2000/svg">
                            <path d="M6 36h12v-4h-12v4zm0-24v4h36v-4h-36zm0 14h24v-4h-24v4z" fill="#757575" />
                            <path d="M0 0h48v48h-48z" fill="none" />
                        </svg>
                    </div>
                </div>
            </div>
            <!-- link to all projects -->
            <div>
                <a href="#" class=" font-[400] text-[#4489FE] text-[14px] leading-[16.41px] float-right font-roboto underline">All
                    Projects</a>
            </div>
        </div>
        <!-- list -->
        <div>
            <div class="overflow-x-auto relative ">
                <table class="  border-collapse w-full text-left ">
                    <thead class=" h-[53.5px]  text-[12px] text-[#212121] font-medium font-roboto  border-b ">
                        <tr>
                            <th scope="col" class="w-[212px] ">Project Name</th>
                            <th scope="col" class="w-[201px] ">Client</th>
                            <th scope="col" class="w-[87px] ">Staff</th>
                        </tr>
                    </thead>
                    <tbody>
                        <tr class=" h-[53.5px] hover:bg-gray-50 ">
                            <td scope="row" 
                                class=" py-0  w-[212px] font-[400] text-[14px] leading-[16.41px] text-[#212121] font-roboto  whitespace-nowrap ">
                                <div class="flex ">
                                    <span class="mr-[7px]"> Ukrainian Transcription</span>
                                    
                                        <svg xmlns="http://www.w3.org/2000/svg" class="h-[15px] w-[15px] text-[#4489fe] cursor-pointer"
                                            fill="none" viewBox="0 0 24 24" stroke="currentColor" stroke-width="2">
                                            <path stroke-linecap="round" stroke-linejoin="round"
                                                d="M10 6H6a2 2 0 00-2 2v10a2 2 0 002 2h10a2 2 0 002-2v-4M14 4h6m0 0v6m0-6L10 14" />
                                        </svg>

                                  
                                </div>
                            </td>
                            <td class=" py-0 w-[201px]">
                                <div class="flex items-center w-[186px] ">
                                    <div class="flex-none">
                                        <img type="button" class="w-[30px] h-[30px] rounded-full  cursor-pointer mr-[10px] "
                                            src="profil.jpeg" alt="User Name" />
                                    </div>

                                    <div class=" ">
                                        <div
                                            class="font-roboto transform translate-y-[1px] text-[11px] leading-[20px] text-[#212121] ">
                                            Serhii
                                            Movchan</div>
                                        <div
                                            class="font-roboto transform  -translate-y-[4.63px] text-[11px] leading-[20px] text-[#BDBDBD]">
                                            example@gmail.com</div>
                                    </div>
                                </div>
                            </td>
                            <td class=" py-0 pl-[15px] w-[87px]">
                                <div class="flex -space-x-[12px] flex-none w-[86.67px]">
                                    <img class="w-[29.63px] h-[29.63px] rounded-full border-[3px] border-white "
                                        src="profil.jpeg" alt="" />
                                    <img class="w-[29.63px] h-[29.63px] rounded-full border-[3px] border-white "
                                        src="profil.jpeg" alt="" />
                                    <img class="w-[29.63px] h-[29.63px] rounded-full border-[3px] border-white "
                                        src="profil.jpeg" alt="" />
                                        <a class="flex justify-center items-center w-[29.63px] h-[29.63px] text-xs font-medium text-[#818181] bg-[#DBDBDB] rounded-full border-2 border-white hover:bg-gray-600 "
                                        href="#">+5</a>
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
    name: "ProjectListSide",
};
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

.external {
    width: 20px;
    height: 20px;
    color: #4489fe;
    padding-left: 7px;
    cursor: pointer;
}


.avatar-background {
    background: #dbdbdb;
}
</style>
