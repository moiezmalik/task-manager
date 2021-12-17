<template>
  <div class="home">
    <div class="container">
      <div class="row">
        <div class="col-md-6 offset-md-3">
          <div class="card bg-light">
            <div class="card-head">
              <Head title="Task App" logo="/img/Moiez-Malik.5be7a4c5.png" />
            </div>
            <div class="card-body">
              <TaskForm />
              <TasksList @delete-task="deleteTask" :tasks="tasks" />
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script lang="ts">
import { Options, Vue } from "vue-class-component";
import Head from "@/components/head.vue";
import TaskForm from "@/components/tasksForm.vue";
import TasksList from "@/components/tasksList.vue";

@Options({
  components: {
    Head,
    TaskForm,
    TasksList,
  },
  data() {
    return {
      tasks: [],
    };
  },
  methods: {
    deleteTask(id: any) {
      console.log(id);
        this.tasks = this.tasks.filter((task: any) => task.id !== id)
      }
  },
  created() {
    this.tasks = [
      {
        id: 1,
        title: "Doctor's Appointment",
        description: "Meet doctor Chang at 12pm",
        reminder: true,
      },
      {
        id: 2,
        title: "Car Appointment",
        description: "Meet mechanic Chang at 12pm",
        reminder: false,
      },
      {
        id: 3,
        title: "Prof's Appointment",
        description: "Meet prof Mike at 12pm",
        reminder: true,
      },
    ];
  },
})
export default class Home extends Vue {}
</script>

<style>
</style>
