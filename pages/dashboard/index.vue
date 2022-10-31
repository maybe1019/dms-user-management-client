<template>
  <div>
    <div>
      <DashNavBar />
    </div>

    <!-- body containner -->
    <div class="flex flex-col justify-between mycontainer pt-12">
      <section>
        <DashStatBrick />
      </section>
      <section class="w-full myStat">
        <Stat />
      </section>
      <!-- project and task llist -->
      <section class="flex flex-row flex-wrap justify-between">
        <div><ProjectListSide /></div>
        <div><TaskListSide /></div>
      </section>
      <section class="mt-1">
        <hr />
        <BottomSection />
      </section>
    </div>
  </div>
</template>

<script>
import DashNavBar from "../../components/nourrisson/DashNavBar.vue";
import BottomSection from "../../components/foeutus/BottomSection.vue";
import DashStatBrick from "../../components/nourrisson/BrickStatStack.vue";
import Stat from "../../components/foeutus/StatGraph.vue";
import ProjectListSide from "../../components/nourrisson/ProjectListSIde.vue";
import TaskListSide from "../../components/nourrisson/TaskListSide.vue";
export default {
  name: "IndexPage",
  components: {
    DashNavBar,
    BottomSection,
    DashStatBrick,
    Stat,
    ProjectListSide,
    TaskListSide,
  },
};
</script>

<style scoped>
.mycontainer {
  margin-left: 8%;
  margin-right: 8%;
}
.myStat {
  height: 40%;
}
.project-info {
  transform: translateY(-30px);
}
@media screen and (max-width: 900px) {
  .mycontainer {
    margin-left: 1rem;
    margin-right: 1rem;
  }
}
</style>
