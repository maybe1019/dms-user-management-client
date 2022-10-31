<template>
	<div class="border py-[45px] px-[38px]   mb-[49px] w-full rounded-[4px]">
		<div class="font-[400] font-roboto text-[24px] leading-[28.13px]">
			Permissions
		</div>
		<table class="w-full text-sm border-collapse mt-[55px]   text-left ">
			<thead class=" ">
				<tr
					class="border-none leading-[14.06px] text-[#212121] text-[12px] font-roboto font-medium">

					<th scope="col" class="py-[21px] !pl-[15px]  w-[252px] ">
						
							Page Name
						
						
					</th>
					<th scope="col" class="py-[21px]  w-[83.2px]">
						View

						
					</th>
					<th scope="col" class="py-[21px] w-[83.2px] ">
				Use

						
					</th>
					<th scope="col" class="py-[21px]  w-[82.62px] ">
					Create

						
					</th>
					<th scope="col" class="py-[21px] w-[83px] ">
						Edit

						
					</th>
					<th scope="col" class="py-[21px]  w-[83px] ">
					 Delete

						
					</th>
					<th scope="col" class="py-[21px] w-[67px]">
						All

						
					</th>
				</tr>
			</thead>

			<tbody>
				<tr class="   hover:bg-gray-50 h-[60px]   ">

					<td
						class=" border-l-0 py-0 !pl-[15px] w-[252px] text-[#212121] font-roboto font-[400] leading-[16.41px]">
						
							Order amount

						
					</td>
					<td class="py-0  w-[83.2px]">
						
							<CheckBox :checkType="'determinate'" :checked="true" />

					

					</td>

					<td class="py-0  w-[83.2px] ">
						
							<CheckBox :checkType="'determinate'" :checked="true" />

						

					</td>
					<td class="py-0  w-[82.62px] ">
						
							<CheckBox :checkType="'determinate'" :checked="true" />

						

					</td>
					<td class="py-0 w-[83px]  ">
						
							<CheckBox :checkType="'determinate'" />

						

					</td>
					<td class="py-0  w-[83px] ">
							<CheckBox :checkType="'determinate'" />


					</td>
					<td class="py-0  border-r-0  w-[67px]  ">
							<CheckBox :checkType="'determinate'" />


					</td>

				</tr>




				





			</tbody>
		</table>

		<div class=" flex  items-center justify-center space-x-[10px] mt-[48px] mb-[49px] ">

			<button class=" shadow-none text-center w-[200px] h-[50px] font-medium bg-[#4489FE]   font-roboto  text-[14px] text-[#FFFFFF] rounded-[4px] outline-none focus:outline-none mr-1 mb-1 transition-all duration-150"
				type="button">
				Save as Role
			</button>
		</div>

	</div>
</template>

<script>
import CheckBox from '../../embrillons/CheckBox.vue';
export default {
	name: 'Permissiom',
	components: {
		CheckBox
	}
}
</script>

<style scoped>
	tr th,
tr td {
   
    padding-right: 0px ;
    padding-left: 0px;

}
</style>
