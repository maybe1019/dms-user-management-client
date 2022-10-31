<template>
       <div v-on:click="setState"
              class="  cursor-pointer  w-[14px] h-[14px] bg-white  border-[#DEE0E4] border-[1px]  rounded-[2px] p-[2px]"
             >
             <div  v-bind:class="{ 'mybg border-[#DEE0E4] w-[8px] h-[8px] rounded-[2px]': (isChecked === true), 'bg-white': (isChecked === false) }" >

             </div>


       </div>
</template>
<script>

export default {
       name: "LoginCheckBox",
       props: {
              checked: {
                     type: Boolean
              },
             
       },
       data() {
              return ({
                     isChecked: false,
                     indType: true
              })
       },
       async mounted() {
              await this.$nextTick();
              if (this.checked) {
                     this.isChecked = true
              }
       }
       ,
       methods: {
              setState() {
                     
                            this.isChecked = !this.isChecked


                    

              }

       }
};
</script>
<style scoped>
.mybg {
       background-color: #4489FE;
}
</style>
