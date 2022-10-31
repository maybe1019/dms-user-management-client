<template>
  <div>
    <PrincipalNavBarVue />
    <div>
      <SetupText />
    </div>
    <div class="mx-12">
      <div class="flex items-start justify-between">
        <AddServices />
        <ServiceInformations />
      </div>

      <div class="flex justify-end py-5">
        <NextButton />
      </div>
      <hr />
      <div class="mb-0">
<BottomSection/>

      </div>

      
    </div>
  </div>
</template>

<script>
import PrincipalNavBarVue from "../../components/nourrisson/PrincipalNavBar.vue";
import SetupText from "../../components/embrillons/SetupText.vue";
import AddServices from "../../components/foeutus/AddServices.vue";
import ServiceInformations from "../../components/foeutus/ServiceInformations.vue";
import NextButton from "../../components/embrillons/NextButon.vue";
import BottomSection from "../../components/foeutus/BottomSection.vue";
export default {
  name: "IndexPage",
  components: {
    PrincipalNavBarVue,
    SetupText,
    AddServices,
    ServiceInformations,
    NextButton,
    BottomSection,
  },
};
</script>
