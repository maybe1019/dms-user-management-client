<template>
<div class="flex w-full max-w-[1440px] space-x-[245px] mx-auto   ">
       <div class=" w-full max-w-[475px]  sm:hidden" >
              <ImageFront/>
       </div>
       <div class=" w-full max-w-[965px] sm:w-full my-auto mx-auto ">
              <LoginForm/>
       </div>
</div>
</template>
<script>
import ImageFront from '../../components/foeutus/login/ImageFront.vue';
import LoginForm from '../../components/foeutus/login/LoginForm.vue';
export default {
       name: "Login",
       components:{
    ImageFront,
    LoginForm,
}
};
</script>
<style scoped></style>
